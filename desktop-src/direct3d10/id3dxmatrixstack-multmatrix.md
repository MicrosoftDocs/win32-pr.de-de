---
description: Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: 'ID3DXMATRIXStack:: mehrtmatrix-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrix
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 43f80ca26f615e02570f0855b1ba6c2435e11b5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360241"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="93056-103">ID3DXMATRIXStack:: mehrtmatrix-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="93056-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="93056-104">Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="93056-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="93056-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93056-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="93056-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="93056-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93056-107">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93056-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93056-108">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="93056-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="93056-109">Ein Zeiger auf die D3DXMATRIX-Struktur, die mit der aktuellen Matrix multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="93056-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93056-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93056-110">Return value</span></span>

<span data-ttu-id="93056-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93056-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93056-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93056-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="93056-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="93056-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="93056-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="93056-114">Remarks</span></span>

<span data-ttu-id="93056-115">Diese Methode multipliziert die angegebene Matrix nach rechts mit der aktuellen Matrix (die Transformation geht zum aktuellen Ursprung der Welt).</span><span class="sxs-lookup"><span data-stu-id="93056-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="93056-116">Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="93056-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="93056-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93056-117">Requirements</span></span>



| <span data-ttu-id="93056-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93056-118">Requirement</span></span> | <span data-ttu-id="93056-119">Wert</span><span class="sxs-lookup"><span data-stu-id="93056-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93056-120">Header</span><span class="sxs-lookup"><span data-stu-id="93056-120">Header</span></span><br/>  | <dl> <span data-ttu-id="93056-121"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="93056-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="93056-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="93056-122">Library</span></span><br/> | <dl> <span data-ttu-id="93056-123"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93056-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93056-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93056-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93056-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="93056-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="93056-126">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="93056-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
