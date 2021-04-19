---
description: Zerstört die Teilstruktur von Frames unter dem Stamm, einschließlich des Stamms.
ms.assetid: 0bbb529f-01d8-430b-a72b-4af5f7a71253
title: D3DXFrameDestroy-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameDestroy
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1c0809ff61abec6f55564ca17a116ad4c826bca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355808"
---
# <a name="d3dxframedestroy-function"></a><span data-ttu-id="5a206-103">D3DXFrameDestroy-Funktion</span><span class="sxs-lookup"><span data-stu-id="5a206-103">D3DXFrameDestroy function</span></span>

<span data-ttu-id="5a206-104">Zerstört die Teilstruktur von Frames unter dem Stamm, einschließlich des Stamms.</span><span class="sxs-lookup"><span data-stu-id="5a206-104">Destroys the subtree of frames under the root, including the root.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a206-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a206-105">Syntax</span></span>


```C++
HRESULT D3DXFrameDestroy(
  _In_ LPD3DXFRAME             pFrameRoot,
  _In_ LPD3DXALLOCATEHIERARCHY pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="5a206-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a206-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a206-107">*pframeroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a206-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a206-108">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="5a206-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="5a206-109">Zeiger auf den Stamm Knoten.</span><span class="sxs-lookup"><span data-stu-id="5a206-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="5a206-110">*palloc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a206-110">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a206-111">Typ: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="5a206-111">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="5a206-112">Zuordnungs Schnittstelle zum Aufheben der Zuordnung von Knoten der Frame Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="5a206-112">Allocation interface used to deallocate nodes of the frame hierarchy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a206-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a206-113">Return value</span></span>

<span data-ttu-id="5a206-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a206-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a206-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a206-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5a206-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="5a206-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a206-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a206-117">Requirements</span></span>



| <span data-ttu-id="5a206-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a206-118">Requirement</span></span> | <span data-ttu-id="5a206-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5a206-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a206-120">Header</span><span class="sxs-lookup"><span data-stu-id="5a206-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5a206-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a206-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5a206-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a206-122">Library</span></span><br/> | <dl> <span data-ttu-id="5a206-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a206-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a206-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a206-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a206-125">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="5a206-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




