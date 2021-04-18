---
description: Bestimmt das Produkt der aktuellen Matrix und die berechnete Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.
ms.assetid: e0ac72a2-9970-433e-9026-aa79edc8261c
title: 'ID3DXMATRIXStack:: Translation-Methode (D3dx9math. h)'
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
ms.openlocfilehash: 228b4302a512e96d5c009edcb3f0b673ee61e047
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365873"
---
# <a name="id3dxmatrixstacktranslate-method-d3dx9mathh"></a><span data-ttu-id="2b5d1-103">ID3DXMATRIXStack:: Translation-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2b5d1-103">ID3DXMATRIXStack::Translate method (D3dx9math.h)</span></span>

<span data-ttu-id="2b5d1-104">Bestimmt das Produkt der aktuellen Matrix und die berechnete Übersetzungs Matrix, die durch die angegebenen Faktoren (x, y und z) bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="2b5d1-104">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b5d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b5d1-105">Syntax</span></span>


```C++
HRESULT Translate(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="2b5d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b5d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b5d1-107">*x* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b5d1-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5d1-108">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5d1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b5d1-109">Der Übersetzungs Faktor in der x-Richtung.</span><span class="sxs-lookup"><span data-stu-id="2b5d1-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="2b5d1-110">*j* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b5d1-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5d1-111">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5d1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b5d1-112">Der Übersetzungs Faktor in y-Richtung.</span><span class="sxs-lookup"><span data-stu-id="2b5d1-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="2b5d1-113">*z* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b5d1-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5d1-114">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b5d1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b5d1-115">Der Übersetzungs Faktor in der z-Richtung.</span><span class="sxs-lookup"><span data-stu-id="2b5d1-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b5d1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b5d1-116">Return value</span></span>

<span data-ttu-id="2b5d1-117">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b5d1-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b5d1-118">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2b5d1-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b5d1-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b5d1-119">Remarks</span></span>

<span data-ttu-id="2b5d1-120">Mit dieser Methode wird die aktuelle Matrix mit der berechneten Übersetzungs Matrix nach rechts multipliziert (die Transformation geht um den aktuellen Ursprung der Welt).</span><span class="sxs-lookup"><span data-stu-id="2b5d1-120">This method right-multiplies the current matrix with the computed translation matrix (transformation is about the current world origin).</span></span>


```
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = m_stack[m_currentPos] * tmp;
```



## <a name="requirements"></a><span data-ttu-id="2b5d1-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b5d1-121">Requirements</span></span>



| <span data-ttu-id="2b5d1-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b5d1-122">Requirement</span></span> | <span data-ttu-id="2b5d1-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2b5d1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b5d1-124">Header</span><span class="sxs-lookup"><span data-stu-id="2b5d1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2b5d1-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b5d1-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2b5d1-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b5d1-126">Library</span></span><br/> | <dl> <span data-ttu-id="2b5d1-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b5d1-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2b5d1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b5d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b5d1-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="2b5d1-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="2b5d1-130">**ID3DXMATRIXStack:: translatelocal**</span><span class="sxs-lookup"><span data-stu-id="2b5d1-130">**ID3DXMATRIXStack::TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)
</dt> </dl>

 

 
