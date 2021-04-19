---
description: Interpoliert zwischen Quaternionen mithilfe der sphärischen Quadranten-Interpolation.
ms.assetid: afce9afb-64cc-4059-90f5-7ed1aca9b3cb
title: D3DXQuaternionSquad-Funktion (D3dx9math. h)
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
ms.openlocfilehash: 3e4fa980d551ac43f66035c1dcaa46d1c1c590a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361857"
---
# <a name="d3dxquaternionsquad-function-d3dx9mathh"></a><span data-ttu-id="2f010-103">D3DXQuaternionSquad-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2f010-103">D3DXQuaternionSquad function (D3dx9math.h)</span></span>

<span data-ttu-id="2f010-104">Interpoliert zwischen Quaternionen mithilfe der sphärischen Quadranten-Interpolation.</span><span class="sxs-lookup"><span data-stu-id="2f010-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f010-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f010-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2f010-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f010-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f010-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="2f010-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f010-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f010-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f010-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="2f010-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2f010-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f010-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f010-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f010-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f010-112">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f010-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f010-113">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f010-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f010-114">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f010-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f010-115">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f010-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f010-116">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f010-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f010-117">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f010-117">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f010-118">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f010-118">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f010-119">*PC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f010-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f010-120">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="2f010-120">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f010-121">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2f010-121">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="2f010-122">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f010-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f010-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f010-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f010-124">-Parameter, der angibt, wie weit zwischen den Quaternionen interpolieren werden soll.</span><span class="sxs-lookup"><span data-stu-id="2f010-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f010-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f010-125">Return value</span></span>

<span data-ttu-id="2f010-126">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f010-126">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="2f010-127">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis der sphärischen Quadrangle-interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="2f010-127">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f010-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f010-128">Remarks</span></span>

<span data-ttu-id="2f010-129">Diese Funktion verwendet die folgende Sequenz von sphärischen linearen Interpolations Vorgängen:</span><span class="sxs-lookup"><span data-stu-id="2f010-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="2f010-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2f010-130">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2f010-131">Auf diese Weise kann die **D3DXQuaternionSquad** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f010-131">In this way, the **D3DXQuaternionSquad** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="2f010-132">Ein Beispiel für die Interpolation zwischen Quaternionen finden Sie im Beispiel skinnedmesh.</span><span class="sxs-lookup"><span data-stu-id="2f010-132">For an example of interpolating between quaternions, see the SkinnedMesh Sample.</span></span> <span data-ttu-id="2f010-133">Dieses Beispiel finden Sie im DirectX SDK.</span><span class="sxs-lookup"><span data-stu-id="2f010-133">You can get this sample and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="2f010-134">Weitere Informationen zum DirectX SDK finden Sie unter [wo ist das DirectX SDK?](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="2f010-134">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="2f010-135">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="2f010-135">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f010-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f010-136">Requirements</span></span>



| <span data-ttu-id="2f010-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f010-137">Requirement</span></span> | <span data-ttu-id="2f010-138">Wert</span><span class="sxs-lookup"><span data-stu-id="2f010-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f010-139">Header</span><span class="sxs-lookup"><span data-stu-id="2f010-139">Header</span></span><br/>  | <dl> <span data-ttu-id="2f010-140"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f010-140"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2f010-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2f010-141">Library</span></span><br/> | <dl> <span data-ttu-id="2f010-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f010-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f010-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f010-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f010-144">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="2f010-144">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2f010-145">**D3DXQuaternionExp**</span><span class="sxs-lookup"><span data-stu-id="2f010-145">**D3DXQuaternionExp**</span></span>](d3dxquaternionexp.md)
</dt> <dt>

[<span data-ttu-id="2f010-146">**D3DXQuaternionLn**</span><span class="sxs-lookup"><span data-stu-id="2f010-146">**D3DXQuaternionLn**</span></span>](d3dxquaternionln.md)
</dt> <dt>

[<span data-ttu-id="2f010-147">**D3DXQuaternionSquadSetup**</span><span class="sxs-lookup"><span data-stu-id="2f010-147">**D3DXQuaternionSquadSetup**</span></span>](d3dxquaternionsquadsetup.md)
</dt> </dl>

 

 
