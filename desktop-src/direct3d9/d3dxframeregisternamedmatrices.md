---
description: Bei einer Frame Hierarchie registriert alle benannten Matrizen im Animations Mixer.
ms.assetid: df0560c2-4417-4d54-94c8-031521b32189
title: D3DXFrameRegisterNamedMatrices-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameRegisterNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8496f467e668939c5d5aa0e90266ab012d436038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366464"
---
# <a name="d3dxframeregisternamedmatrices-function"></a><span data-ttu-id="74097-103">D3DXFrameRegisterNamedMatrices-Funktion</span><span class="sxs-lookup"><span data-stu-id="74097-103">D3DXFrameRegisterNamedMatrices function</span></span>

<span data-ttu-id="74097-104">Bei einer Frame Hierarchie registriert alle benannten Matrizen im Animations Mixer.</span><span class="sxs-lookup"><span data-stu-id="74097-104">Given a frame hierarchy, registers all the named matrices in the animation mixer.</span></span>

## <a name="syntax"></a><span data-ttu-id="74097-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74097-105">Syntax</span></span>


```C++
HRESULT D3DXFrameRegisterNamedMatrices(
  _In_ LPD3DXFRAME               pFrameRoot,
  _In_ LPD3DXANIMATIONCONTROLLER pAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="74097-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="74097-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74097-107">*pframeroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74097-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74097-108">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="74097-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="74097-109">Der Knoten der obersten Ebene in der Frame Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="74097-109">The top level node in the frame hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="74097-110">*panimcontroller* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74097-110">*pAnimController* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74097-111">Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span><span class="sxs-lookup"><span data-stu-id="74097-111">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**</span></span>

<span data-ttu-id="74097-112">Zeiger auf das Animations Controller Objekt.</span><span class="sxs-lookup"><span data-stu-id="74097-112">Pointer to the animation controller object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74097-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74097-113">Return value</span></span>

<span data-ttu-id="74097-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74097-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74097-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74097-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74097-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="74097-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="74097-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74097-117">Requirements</span></span>



| <span data-ttu-id="74097-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74097-118">Requirement</span></span> | <span data-ttu-id="74097-119">Wert</span><span class="sxs-lookup"><span data-stu-id="74097-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74097-120">Header</span><span class="sxs-lookup"><span data-stu-id="74097-120">Header</span></span><br/>  | <dl> <span data-ttu-id="74097-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="74097-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="74097-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="74097-122">Library</span></span><br/> | <dl> <span data-ttu-id="74097-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74097-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74097-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74097-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74097-125">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="74097-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




