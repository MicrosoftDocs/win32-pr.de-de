---
description: 'D3DXMatrixDecompose-Funktion (D3DX10Math.h): Unterteilt eine allgemeine 3D-Transformationsmatrix in ihre skalaren, rotationsbasierten und translationalen Komponenten.'
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: D3DXMatrixDecompose-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixDecompose
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cc87de99d72283c20f25b15ea8d0e5864e2550d9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113208"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="1bba8-103">D3DXMatrixDecompose-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="1bba8-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="1bba8-104">Unterteilt eine allgemeine 3D-Transformationsmatrix in ihre skalaren, rotations- und translationalen Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1bba8-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bba8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1bba8-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="1bba8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1bba8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bba8-107">*pOutScale* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1bba8-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bba8-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bba8-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1bba8-109">Zeiger auf die [**D3DXVECTOR3-Ausgabe,**](d3d10-d3dxvector3.md) die Skalierungsfaktoren enthält, die auf die x-, y- und z-Achse angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bba8-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="1bba8-110">*pOutRotation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1bba8-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bba8-111">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bba8-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="1bba8-112">Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) der die Drehung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1bba8-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="1bba8-113">*pOutTranslation* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1bba8-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bba8-114">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1bba8-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1bba8-115">Zeiger auf den D3DXVECTOR3-Vektor, der die Übersetzung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1bba8-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="1bba8-116">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="1bba8-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bba8-117">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1bba8-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1bba8-118">Zeiger auf eine zu zerlegende [**D3DXMATRIX-Eingabematrix.**](d3d10-d3dxmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="1bba8-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bba8-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1bba8-119">Return value</span></span>

<span data-ttu-id="1bba8-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1bba8-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1bba8-121">Wenn die Funktion erfolgreich ist, lautet der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1bba8-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1bba8-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt sein: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1bba8-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bba8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bba8-123">Requirements</span></span>



| <span data-ttu-id="1bba8-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1bba8-124">Requirement</span></span> | <span data-ttu-id="1bba8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1bba8-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1bba8-126">Header</span><span class="sxs-lookup"><span data-stu-id="1bba8-126">Header</span></span><br/>  | <dl> <span data-ttu-id="1bba8-127"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="1bba8-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="1bba8-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1bba8-128">Library</span></span><br/> | <dl> <span data-ttu-id="1bba8-129"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="1bba8-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1bba8-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1bba8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bba8-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1bba8-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
