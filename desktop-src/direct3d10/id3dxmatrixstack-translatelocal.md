---
description: 'ID3DXMATRIXStack::TranslateLocal-Methode (D3DX10.h): Bestimmt das Produkt der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.'
ms.assetid: 96399801-dd80-4e9a-a5c3-c5d41eb9368a
title: ID3DXMATRIXStack::TranslateLocal-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80fabea58bd30b0db9b3ff41b522614007fe4b7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107748"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx10h"></a><span data-ttu-id="285a0-103">ID3DXMATRIXStack::TranslateLocal-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="285a0-103">ID3DXMATRIXStack::TranslateLocal method (D3DX10.h)</span></span>

<span data-ttu-id="285a0-104">Bestimmt das Produkt der berechneten Übersetzungsmatrix, die durch die angegebenen Faktoren (x, y und z) und die aktuelle Matrix bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="285a0-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="285a0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="285a0-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="285a0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="285a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="285a0-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="285a0-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="285a0-108">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="285a0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="285a0-109">Der Übersetzungsfaktor in x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="285a0-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="285a0-110">*y* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="285a0-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="285a0-111">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="285a0-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="285a0-112">Der Übersetzungsfaktor in der y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="285a0-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="285a0-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="285a0-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="285a0-114">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="285a0-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="285a0-115">Der Übersetzungsfaktor in der Z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="285a0-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="285a0-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="285a0-116">Return value</span></span>

<span data-ttu-id="285a0-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="285a0-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="285a0-118">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="285a0-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="285a0-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="285a0-119">Remarks</span></span>

<span data-ttu-id="285a0-120">Diese Methode multipliziert die aktuelle Matrix mit der berechneten Übersetzungsmatrix (die Transformation bezieht sich auf den lokalen Ursprung des Objekts).</span><span class="sxs-lookup"><span data-stu-id="285a0-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation(&tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="285a0-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="285a0-121">Requirements</span></span>



| <span data-ttu-id="285a0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="285a0-122">Requirement</span></span> | <span data-ttu-id="285a0-123">Wert</span><span class="sxs-lookup"><span data-stu-id="285a0-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="285a0-124">Header</span><span class="sxs-lookup"><span data-stu-id="285a0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="285a0-125"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="285a0-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="285a0-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="285a0-126">Library</span></span><br/> | <dl> <span data-ttu-id="285a0-127"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="285a0-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="285a0-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="285a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="285a0-129">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="285a0-129">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="285a0-130">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="285a0-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
