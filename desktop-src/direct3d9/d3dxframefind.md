---
description: Sucht den untergeordneten Rahmen eines Stamm Frames.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: D3DXFrameFind-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361206"
---
# <a name="d3dxframefind-function"></a><span data-ttu-id="f2da5-103">D3DXFrameFind-Funktion</span><span class="sxs-lookup"><span data-stu-id="f2da5-103">D3DXFrameFind function</span></span>

<span data-ttu-id="f2da5-104">Sucht den untergeordneten Rahmen eines Stamm Frames.</span><span class="sxs-lookup"><span data-stu-id="f2da5-104">Finds the child frame of a root frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2da5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2da5-105">Syntax</span></span>


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a><span data-ttu-id="f2da5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2da5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2da5-107">*pframeroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2da5-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2da5-108">Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="f2da5-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="f2da5-109">Zeiger auf den stammframe.</span><span class="sxs-lookup"><span data-stu-id="f2da5-109">Pointer to the root frame.</span></span> <span data-ttu-id="f2da5-110">Siehe [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="f2da5-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="f2da5-111">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2da5-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2da5-112">Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f2da5-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f2da5-113">Der Name des zu suchenden untergeordneten Frames.</span><span class="sxs-lookup"><span data-stu-id="f2da5-113">Name of the child frame to find.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2da5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2da5-114">Return value</span></span>

<span data-ttu-id="f2da5-115">Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="f2da5-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="f2da5-116">Gibt den untergeordneten Frame zurück, wenn er gefunden wird, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="f2da5-116">Returns the child frame if it is found, or **NULL** otherwise.</span></span> <span data-ttu-id="f2da5-117">Siehe [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="f2da5-117">See [**D3DXFRAME**](d3dxframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2da5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f2da5-118">Requirements</span></span>



| <span data-ttu-id="f2da5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f2da5-119">Requirement</span></span> | <span data-ttu-id="f2da5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f2da5-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2da5-121">Header</span><span class="sxs-lookup"><span data-stu-id="f2da5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f2da5-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2da5-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f2da5-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f2da5-123">Library</span></span><br/> | <dl> <span data-ttu-id="f2da5-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f2da5-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f2da5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2da5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2da5-126">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="f2da5-126">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
