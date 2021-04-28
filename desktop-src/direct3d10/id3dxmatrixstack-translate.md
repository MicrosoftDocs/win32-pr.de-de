---
description: 'ID3DXMATRIXStack::Translate-Methode (D3DX10.h): Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.'
ms.assetid: d6e347a5-bb66-451d-b66e-49ea8eff70b3
title: ID3DXMATRIXStack::Translate-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.Translate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 41e84b62c077da03806a5e781498c05ee3c8ee67
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107768"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx10h"></a><span data-ttu-id="f295d-103">ID3DXMATRIXStack::Translate-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="f295d-103">ID3DXMATRIXStack::Translate method (D3DX10.h)</span></span>

<span data-ttu-id="f295d-104">Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="f295d-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="f295d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f295d-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="f295d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f295d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f295d-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f295d-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f295d-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f295d-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f295d-109">Der Übersetzungsfaktor in x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="f295d-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f295d-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f295d-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f295d-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f295d-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f295d-112">Der Übersetzungsfaktor in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="f295d-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="f295d-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f295d-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f295d-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f295d-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f295d-115">Der Übersetzungsfaktor in der Z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="f295d-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f295d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f295d-116">Return value</span></span>

<span data-ttu-id="f295d-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f295d-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f295d-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f295d-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f295d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f295d-119">Remarks</span></span>

<span data-ttu-id="f295d-120">Diese Methode multipliziert die aktuelle Matrix mit der berechneten Übersetzungsmatrix (die Transformation bezieht sich auf den aktuellen Ursprung der Welt).</span><span class="sxs-lookup"><span data-stu-id="f295d-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="f295d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f295d-121">Requirements</span></span>



| <span data-ttu-id="f295d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f295d-122">Requirement</span></span> | <span data-ttu-id="f295d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="f295d-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f295d-124">Header</span><span class="sxs-lookup"><span data-stu-id="f295d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="f295d-125"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="f295d-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f295d-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f295d-126">Library</span></span><br/> | <dl> <span data-ttu-id="f295d-127"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f295d-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f295d-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f295d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f295d-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f295d-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="f295d-130">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f295d-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
