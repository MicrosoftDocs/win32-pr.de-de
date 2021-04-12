---
description: Fügt einem Frame einen untergeordneten Frame hinzu.
ms.assetid: a04c9bbe-8e54-467a-8e02-27c6469f4dac
title: D3DXFrameAppendChild-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameAppendChild
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a27c8b31abf982c7cfaaa2a53d49d8859fa2c8bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219513"
---
# <a name="d3dxframeappendchild-function"></a><span data-ttu-id="cf226-103">D3DXFrameAppendChild-Funktion</span><span class="sxs-lookup"><span data-stu-id="cf226-103">D3DXFrameAppendChild function</span></span>

<span data-ttu-id="cf226-104">Fügt einem Frame einen untergeordneten Frame hinzu.</span><span class="sxs-lookup"><span data-stu-id="cf226-104">Adds a child frame to a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf226-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf226-105">Syntax</span></span>


```C++
HRESULT D3DXFrameAppendChild(
  _In_       LPD3DXFRAME pFrameParent,
  _In_ const D3DXFRAME   *pFrameChild
);
```



## <a name="parameters"></a><span data-ttu-id="cf226-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf226-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf226-107">*pframeparent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf226-107">*pFrameParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf226-108">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="cf226-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="cf226-109">Zeiger auf den übergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="cf226-109">Pointer to the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="cf226-110">*pframechild* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf226-110">*pFrameChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf226-111">Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="cf226-111">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="cf226-112">Zeiger auf den untergeordneten Knoten.</span><span class="sxs-lookup"><span data-stu-id="cf226-112">Pointer to the child node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf226-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf226-113">Return value</span></span>

<span data-ttu-id="cf226-114">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cf226-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cf226-115">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cf226-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cf226-116">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="cf226-116">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf226-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf226-117">Requirements</span></span>



| <span data-ttu-id="cf226-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf226-118">Requirement</span></span> | <span data-ttu-id="cf226-119">Wert</span><span class="sxs-lookup"><span data-stu-id="cf226-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf226-120">Header</span><span class="sxs-lookup"><span data-stu-id="cf226-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cf226-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf226-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="cf226-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf226-122">Library</span></span><br/> | <dl> <span data-ttu-id="cf226-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf226-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf226-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf226-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf226-125">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="cf226-125">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 




