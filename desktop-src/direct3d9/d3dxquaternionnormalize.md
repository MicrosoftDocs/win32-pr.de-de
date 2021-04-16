---
description: Berechnet eine Einheits Längen-Quaternion.
ms.assetid: 31f56c2b-96b0-4110-a5b9-ce09983779b6
title: D3DXQuaternionNormalize-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionNormalize
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d052d4dfc88feb2a00237392071f63d724070b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530890"
---
# <a name="d3dxquaternionnormalize-function-d3dx9mathh"></a><span data-ttu-id="9eb3b-103">D3DXQuaternionNormalize-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9eb3b-103">D3DXQuaternionNormalize function (D3dx9math.h)</span></span>

<span data-ttu-id="9eb3b-104">Berechnet eine Einheits Längen-Quaternion.</span><span class="sxs-lookup"><span data-stu-id="9eb3b-104">Computes a unit length quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eb3b-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionNormalize(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="9eb3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eb3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb3b-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9eb3b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb3b-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9eb3b-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9eb3b-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="9eb3b-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9eb3b-110">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9eb3b-110">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9eb3b-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="9eb3b-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9eb3b-112">Ein Zeiger auf die Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="9eb3b-112">Pointer to the source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb3b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9eb3b-113">Return value</span></span>

<span data-ttu-id="9eb3b-114">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="9eb3b-114">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="9eb3b-115">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die die normale der Quaternion ist.</span><span class="sxs-lookup"><span data-stu-id="9eb3b-115">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the normal of the quaternion.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb3b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9eb3b-116">Remarks</span></span>

<span data-ttu-id="9eb3b-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9eb3b-117">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9eb3b-118">Auf diese Weise kann die **D3DXQuaternionNormalize** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9eb3b-118">In this way, the **D3DXQuaternionNormalize** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb3b-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9eb3b-119">Requirements</span></span>



| <span data-ttu-id="9eb3b-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9eb3b-120">Requirement</span></span> | <span data-ttu-id="9eb3b-121">Wert</span><span class="sxs-lookup"><span data-stu-id="9eb3b-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb3b-122">Header</span><span class="sxs-lookup"><span data-stu-id="9eb3b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9eb3b-123"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9eb3b-123"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9eb3b-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9eb3b-124">Library</span></span><br/> | <dl> <span data-ttu-id="9eb3b-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9eb3b-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9eb3b-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9eb3b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb3b-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9eb3b-127">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="9eb3b-128">**D3DXQuaternionInverse**</span><span class="sxs-lookup"><span data-stu-id="9eb3b-128">**D3DXQuaternionInverse**</span></span>](d3dxquaternioninverse.md)
</dt> </dl>

 

 




