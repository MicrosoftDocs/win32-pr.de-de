---
description: 'ID3DXMATRIXStack::Translate-Methode (D3dx9math.h): Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.'
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: ID3DXMATRIXStack::Translate-Methode (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7fadad95e8e72691a0e030ed89eedc745de2be43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093338"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="e0aa8-103">ID3DXMATRIXStack::Translate-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="e0aa8-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="e0aa8-104">Bestimmt das Produkt der aktuellen Matrix und der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="e0aa8-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="e0aa8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0aa8-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="e0aa8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0aa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0aa8-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0aa8-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0aa8-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0aa8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0aa8-109">Der Übersetzungsfaktor in x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="e0aa8-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="e0aa8-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0aa8-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0aa8-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0aa8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0aa8-112">Der Übersetzungsfaktor in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="e0aa8-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="e0aa8-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0aa8-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0aa8-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e0aa8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e0aa8-115">Der Übersetzungsfaktor in der Z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="e0aa8-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0aa8-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e0aa8-116">Return value</span></span>

<span data-ttu-id="e0aa8-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e0aa8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e0aa8-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e0aa8-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0aa8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0aa8-119">Remarks</span></span>

<span data-ttu-id="e0aa8-120">Diese Methode multipliziert die aktuelle Matrix mit der berechneten Übersetzungsmatrix (die Transformation bezieht sich auf den aktuellen Ursprung der Welt).</span><span class="sxs-lookup"><span data-stu-id="e0aa8-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="e0aa8-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0aa8-121">Requirements</span></span>



| <span data-ttu-id="e0aa8-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0aa8-122">Requirement</span></span> | <span data-ttu-id="e0aa8-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e0aa8-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0aa8-124">Header</span><span class="sxs-lookup"><span data-stu-id="e0aa8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e0aa8-125"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa8-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e0aa8-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0aa8-126">Library</span></span><br/> | <dl> <span data-ttu-id="e0aa8-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0aa8-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e0aa8-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e0aa8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0aa8-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="e0aa8-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="e0aa8-130">**ID3DXMATRIXStack::TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="e0aa8-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
