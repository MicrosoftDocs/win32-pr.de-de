---
description: Unterteilt eine allgemeine 3D-Transformationsmatrix in seine skalaren, rotierenden und Übersetzer Komponenten.
ms.assetid: 3694769f-56e7-4983-924e-021c129462a2
title: D3DXMatrixDecompose-Funktion (D3DX10Math. h)
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
ms.openlocfilehash: 507c8f177db0f71b3d333a8343e4166e649f424a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219665"
---
# <a name="d3dxmatrixdecompose-function-d3dx10mathh"></a><span data-ttu-id="c2bce-103">D3DXMatrixDecompose-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="c2bce-103">D3DXMatrixDecompose function (D3DX10Math.h)</span></span>

<span data-ttu-id="c2bce-104">Unterteilt eine allgemeine 3D-Transformationsmatrix in seine skalaren, rotierenden und Übersetzer Komponenten.</span><span class="sxs-lookup"><span data-stu-id="c2bce-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2bce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2bce-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _In_       D3DXVECTOR3    *pOutScale,
  _In_       D3DXQUATERNION *pOutRotation,
  _In_       D3DXVECTOR3    *pOutTranslation,
  _In_ const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c2bce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2bce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2bce-107">*poutscale* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2bce-107">*pOutScale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bce-108">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2bce-108">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c2bce-109">Zeiger auf das Ausgabe [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , das Skalierungsfaktoren enthält, die auf der x-, y-und z-Achse angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2bce-109">Pointer to the output [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="c2bce-110">*poutrotation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2bce-110">*pOutRotation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bce-111">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2bce-111">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="c2bce-112">Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das die Drehung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c2bce-112">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="c2bce-113">*pouttranslation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2bce-113">*pOutTranslation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bce-114">Typ: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="c2bce-114">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="c2bce-115">Zeiger auf den D3DXVECTOR3-Vektor, der die Übersetzung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c2bce-115">Pointer to the D3DXVECTOR3 vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="c2bce-116">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2bce-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2bce-117">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c2bce-117">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c2bce-118">Zeiger auf eine [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Eingabe Matrix, die zerlegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2bce-118">Pointer to an input [**D3DXMATRIX**](d3d10-d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2bce-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2bce-119">Return value</span></span>

<span data-ttu-id="c2bce-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c2bce-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c2bce-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2bce-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c2bce-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="c2bce-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2bce-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2bce-123">Requirements</span></span>



| <span data-ttu-id="c2bce-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2bce-124">Requirement</span></span> | <span data-ttu-id="c2bce-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c2bce-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2bce-126">Header</span><span class="sxs-lookup"><span data-stu-id="c2bce-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c2bce-127"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2bce-127"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="c2bce-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2bce-128">Library</span></span><br/> | <dl> <span data-ttu-id="c2bce-129"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2bce-129"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c2bce-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2bce-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2bce-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c2bce-131">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
