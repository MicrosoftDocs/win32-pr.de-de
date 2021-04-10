---
description: Zählt die Anzahl von Frames in einer Teilstruktur, die nicht-NULL-Namen aufweisen.
ms.assetid: bc1cb985-acd1-4ba0-bb3c-3e86fea559da
title: D3DXFrameNumNamedMatrices-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameNumNamedMatrices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5c2d535a41d15987df7816cfc23f1bb213b6adc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961602"
---
# <a name="d3dxframenumnamedmatrices-function"></a><span data-ttu-id="a3e7e-103">D3DXFrameNumNamedMatrices-Funktion</span><span class="sxs-lookup"><span data-stu-id="a3e7e-103">D3DXFrameNumNamedMatrices function</span></span>

<span data-ttu-id="a3e7e-104">Zählt die Anzahl von Frames in einer Teilstruktur, die nicht-NULL-Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a3e7e-104">Counts number of frames in a subtree that have non-null names.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3e7e-105">Syntax</span></span>


```C++
UINT D3DXFrameNumNamedMatrices(
  _In_ const D3DXFRAME *pFrameRoot
);
```



## <a name="parameters"></a><span data-ttu-id="a3e7e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3e7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3e7e-107">*pframeroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3e7e-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3e7e-108">Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="a3e7e-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="a3e7e-109">Zeiger auf den Stamm Knoten der Unterstruktur.</span><span class="sxs-lookup"><span data-stu-id="a3e7e-109">Pointer to the root node of the subtree.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3e7e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a3e7e-110">Return value</span></span>

<span data-ttu-id="a3e7e-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a3e7e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a3e7e-112">Gibt die Frame Anzahl zurück.</span><span class="sxs-lookup"><span data-stu-id="a3e7e-112">Returns the frame count.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3e7e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a3e7e-113">Requirements</span></span>



| <span data-ttu-id="a3e7e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a3e7e-114">Requirement</span></span> | <span data-ttu-id="a3e7e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a3e7e-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e7e-116">Header</span><span class="sxs-lookup"><span data-stu-id="a3e7e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a3e7e-117"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3e7e-117"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="a3e7e-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a3e7e-118">Library</span></span><br/> | <dl> <span data-ttu-id="a3e7e-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3e7e-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a3e7e-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3e7e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e7e-121">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3e7e-121">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
