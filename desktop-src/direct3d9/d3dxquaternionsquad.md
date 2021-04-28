---
description: 'D3DXQuaternionSquad-Funktion (D3dx9math.h): Interpolate zwischen Quaternionen mithilfe der pherischen Quadrangleinterpolation.'
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: D3DXQuaternionSquad-Funktion (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c7bef8671b38ec2e8208a6de0ec7542cf28ffa44
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117988"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="21f5e-103">D3DXQuaternionSquad-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="21f5e-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="21f5e-104">Interpoliert zwischen Quaternionen mithilfe der pherischen Quadrangleinterpolation.</span><span class="sxs-lookup"><span data-stu-id="21f5e-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f5e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21f5e-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="21f5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21f5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f5e-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="21f5e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="21f5e-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="21f5e-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="21f5e-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="21f5e-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="21f5e-110">*pQ1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21f5e-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f5e-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="21f5e-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="21f5e-112">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="21f5e-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="21f5e-113">*pA* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21f5e-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f5e-114">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="21f5e-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="21f5e-115">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="21f5e-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="21f5e-116">*pB* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21f5e-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f5e-117">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="21f5e-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="21f5e-118">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="21f5e-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="21f5e-119">*pC* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="21f5e-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f5e-120">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="21f5e-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="21f5e-121">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="21f5e-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="21f5e-122">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21f5e-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21f5e-123">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21f5e-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="21f5e-124">Parameter, der angibt, wie weit zwischen den Quaternionen interpoliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="21f5e-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f5e-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21f5e-125">Return value</span></span>

<span data-ttu-id="21f5e-126">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="21f5e-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="21f5e-127">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis der sphärischen Quadrangleinterpolation ist.</span><span class="sxs-lookup"><span data-stu-id="21f5e-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f5e-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21f5e-128">Remarks</span></span>

<span data-ttu-id="21f5e-129">Diese Funktion verwendet die folgende Sequenz von sphärischen linearen Interpolationsvorgängen:</span><span class="sxs-lookup"><span data-stu-id="21f5e-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="21f5e-130">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter* zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="21f5e-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="21f5e-131">Auf diese Weise kann die **D3DXQuaternionSquad-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="21f5e-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="21f5e-132">Ein Beispiel für die Interpolation zwischen Quaternionen finden Sie im SkinnedMesh-Beispiel.</span><span class="sxs-lookup"><span data-stu-id="21f5e-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="21f5e-133">Sie erhalten dieses Beispiel und erfahren mehr über das DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="21f5e-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="21f5e-134">Informationen zum DirectX SDK finden Sie unter [Wo befindet sich das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="21f5e-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="21f5e-135">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="21f5e-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="21f5e-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21f5e-136">Requirements</span></span>



| <span data-ttu-id="21f5e-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21f5e-137">Requirement</span></span> | <span data-ttu-id="21f5e-138">Wert</span><span class="sxs-lookup"><span data-stu-id="21f5e-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21f5e-139">Header</span><span class="sxs-lookup"><span data-stu-id="21f5e-139">Header</span></span><br/>  | <dl> <span data-ttu-id="21f5e-140"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="21f5e-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="21f5e-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="21f5e-141">Library</span></span><br/> | <dl> <span data-ttu-id="21f5e-142"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="21f5e-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21f5e-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21f5e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f5e-144">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="21f5e-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="21f5e-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="21f5e-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="21f5e-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="21f5e-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="21f5e-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="21f5e-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
