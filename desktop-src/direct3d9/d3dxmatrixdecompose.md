---
description: Unterteilt eine allgemeine 3D-Transformationsmatrix in seine skalaren, rotierenden und Übersetzer Komponenten.
ms.assetid: 73d3c248-1254-444e-9fd8-4f144424ddb7
title: D3DXMatrixDecompose-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92f120f1c3637216d77a5298b5de219f5605d571
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354398"
---
# <a name="d3dxmatrixdecompose-function-d3dx9mathh"></a><span data-ttu-id="2be62-103">D3DXMatrixDecompose-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2be62-103">D3DXMatrixDecompose function (D3dx9math.h)</span></span>

<span data-ttu-id="2be62-104">Unterteilt eine allgemeine 3D-Transformationsmatrix in seine skalaren, rotierenden und Übersetzer Komponenten.</span><span class="sxs-lookup"><span data-stu-id="2be62-104">Breaks down a general 3D transformation matrix into its scalar, rotational, and translational components.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be62-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2be62-105">Syntax</span></span>


```C++
HRESULT D3DXMatrixDecompose(
  _Inout_       D3DXVECTOR3    *pOutScale,
  _Inout_       D3DXQUATERNION *pOutRotation,
  _Inout_       D3DXVECTOR3    *pOutTranslation,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="2be62-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2be62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be62-107">*poutscale* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2be62-107">*pOutScale* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2be62-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2be62-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2be62-109">Zeiger auf das Ausgabe [**D3DXVECTOR3**](d3dxvector3.md) , das Skalierungsfaktoren enthält, die auf der x-, y-und z-Achse angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2be62-109">Pointer to the output [**D3DXVECTOR3**](d3dxvector3.md) that contains scaling factors applied along the x, y, and z-axes.</span></span>

</dd> <dt>

<span data-ttu-id="2be62-110">*poutrotation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2be62-110">*pOutRotation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2be62-111">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2be62-111">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2be62-112">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die Drehung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2be62-112">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that describes the rotation.</span></span>

</dd> <dt>

<span data-ttu-id="2be62-113">*pouttranslation* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2be62-113">*pOutTranslation* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2be62-114">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="2be62-114">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="2be62-115">Zeiger auf den [**D3DXVECTOR3**](d3dxvector3.md) -Vektor, der die Übersetzung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="2be62-115">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) vector that describes the translation.</span></span>

</dd> <dt>

<span data-ttu-id="2be62-116">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2be62-116">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2be62-117">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2be62-117">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2be62-118">Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Eingabe Matrix, die zerlegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2be62-118">Pointer to an input [**D3DXMATRIX**](d3dxmatrix.md) matrix to decompose.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be62-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2be62-119">Return value</span></span>

<span data-ttu-id="2be62-120">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2be62-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2be62-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2be62-121">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2be62-122">Wenn die Funktion fehlschlägt, kann der Rückgabewert wie folgt lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="2be62-122">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2be62-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2be62-123">Requirements</span></span>



| <span data-ttu-id="2be62-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2be62-124">Requirement</span></span> | <span data-ttu-id="2be62-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2be62-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2be62-126">Header</span><span class="sxs-lookup"><span data-stu-id="2be62-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2be62-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2be62-127"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2be62-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2be62-128">Library</span></span><br/> | <dl> <span data-ttu-id="2be62-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2be62-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2be62-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2be62-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be62-131">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2be62-131">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




