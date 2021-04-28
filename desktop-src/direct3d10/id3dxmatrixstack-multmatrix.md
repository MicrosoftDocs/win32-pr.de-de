---
description: 'ID3DXMATRIXStack::MultMatrix-Methode (D3DX10.h): Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.'
ms.assetid: 72388919-e474-4433-b219-41e2d312848e
title: ID3DXMATRIXStack::MultMatrix-Methode (D3DX10.h)
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
ms.openlocfilehash: 969cdebcee34add15cbf6bbcfbb1048387b2d7e8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107968"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx10h"></a><span data-ttu-id="5b3c7-103">ID3DXMATRIXStack::MultMatrix-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="5b3c7-103">ID3DXMATRIXStack::MultMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="5b3c7-104">Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b3c7-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="5b3c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b3c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b3c7-107">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5b3c7-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b3c7-108">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5b3c7-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5b3c7-109">Zeiger auf die D3DXMATRIX-Struktur, die mit der aktuellen Matrix multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b3c7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b3c7-110">Return value</span></span>

<span data-ttu-id="5b3c7-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5b3c7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5b3c7-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5b3c7-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3c7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5b3c7-114">Remarks</span></span>

<span data-ttu-id="5b3c7-115">Diese Methode multipliziert die gegebene Matrix mit der aktuellen Matrix (die Transformation bezieht sich auf den aktuellen Ursprung der Welt).</span><span class="sxs-lookup"><span data-stu-id="5b3c7-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="5b3c7-116">Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="5b3c7-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b3c7-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b3c7-117">Requirements</span></span>



| <span data-ttu-id="5b3c7-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5b3c7-118">Requirement</span></span> | <span data-ttu-id="5b3c7-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5b3c7-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3c7-120">Header</span><span class="sxs-lookup"><span data-stu-id="5b3c7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5b3c7-121"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="5b3c7-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b3c7-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5b3c7-122">Library</span></span><br/> | <dl> <span data-ttu-id="5b3c7-123"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b3c7-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b3c7-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5b3c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b3c7-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="5b3c7-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5b3c7-126">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="5b3c7-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
