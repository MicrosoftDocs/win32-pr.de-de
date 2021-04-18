---
description: Berechnet die umgebende Kugel aller Netze in der Frame Hierarchie.
ms.assetid: 8c3f5a9e-73ff-4d83-8f85-a3fc2a9a53f7
title: D3DXFrameCalculateBoundingSphere-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameCalculateBoundingSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f10043d2c897bf6ab24c442b8e134f31221c498e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371913"
---
# <a name="d3dxframecalculateboundingsphere-function"></a><span data-ttu-id="393b8-103">D3DXFrameCalculateBoundingSphere-Funktion</span><span class="sxs-lookup"><span data-stu-id="393b8-103">D3DXFrameCalculateBoundingSphere function</span></span>

<span data-ttu-id="393b8-104">Berechnet die umgebende Kugel aller Netze in der Frame Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="393b8-104">Computes the bounding sphere of all the meshes in the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="393b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="393b8-105">Syntax</span></span>


```C++
HRESULT D3DXFrameCalculateBoundingSphere(
  _In_  const D3DXFRAME     *pFrameRoot,
  _Out_       LPD3DXVECTOR3 pObjectCenter,
  _Out_       FLOAT         *pObjectRadius
);
```



## <a name="parameters"></a><span data-ttu-id="393b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="393b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="393b8-107">*pframeroot* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="393b8-107">*pFrameRoot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="393b8-108">Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="393b8-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="393b8-109">Zeiger auf den Stamm Knoten.</span><span class="sxs-lookup"><span data-stu-id="393b8-109">Pointer to the root node.</span></span>

</dd> <dt>

<span data-ttu-id="393b8-110">*pobjectcenter* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="393b8-110">*pObjectCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="393b8-111">Typ: **[ **LPD3DXVECTOR3**](d3dxvector3.md)**</span><span class="sxs-lookup"><span data-stu-id="393b8-111">Type: **[**LPD3DXVECTOR3**](d3dxvector3.md)**</span></span>

<span data-ttu-id="393b8-112">Gibt den Mittelpunkt der umgebenden Kugel zurück.</span><span class="sxs-lookup"><span data-stu-id="393b8-112">Returns the center of the bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="393b8-113">*pobjectradius* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="393b8-113">*pObjectRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="393b8-114">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="393b8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="393b8-115">Gibt den Radius der umgebenden Kugel zurück.</span><span class="sxs-lookup"><span data-stu-id="393b8-115">Returns the radius of the bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="393b8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="393b8-116">Return value</span></span>

<span data-ttu-id="393b8-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="393b8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="393b8-118">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="393b8-118">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="393b8-119">Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="393b8-119">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="393b8-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="393b8-120">Requirements</span></span>



| <span data-ttu-id="393b8-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="393b8-121">Requirement</span></span> | <span data-ttu-id="393b8-122">Wert</span><span class="sxs-lookup"><span data-stu-id="393b8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="393b8-123">Header</span><span class="sxs-lookup"><span data-stu-id="393b8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="393b8-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="393b8-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="393b8-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="393b8-125">Library</span></span><br/> | <dl> <span data-ttu-id="393b8-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="393b8-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="393b8-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="393b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="393b8-128">Animations Funktionen</span><span class="sxs-lookup"><span data-stu-id="393b8-128">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
