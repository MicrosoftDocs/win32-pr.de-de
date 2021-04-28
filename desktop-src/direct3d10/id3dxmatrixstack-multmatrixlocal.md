---
description: 'ID3DXMATRIXStack::MultMatrixLocal-Methode (D3DX10.h): Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.'
ms.assetid: 4d374a7b-99e0-4313-970d-b0e7cf3e97ce
title: ID3DXMATRIXStack::MultMatrixLocal-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.MultMatrixLocal
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4b777bd729810b6fd63bd71def9858203b2ac559
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107948"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx10h"></a><span data-ttu-id="c540c-103">ID3DXMATRIXStack::MultMatrixLocal-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="c540c-103">ID3DXMATRIXStack::MultMatrixLocal method (D3DX10.h)</span></span>

<span data-ttu-id="c540c-104">Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="c540c-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="c540c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c540c-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="c540c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c540c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c540c-107">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="c540c-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c540c-108">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="c540c-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="c540c-109">Zeiger auf die D3DXMATRIX-Struktur, die mit der aktuellen Matrix multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c540c-109">Pointer to the D3DXMATRIX structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c540c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c540c-110">Return value</span></span>

<span data-ttu-id="c540c-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c540c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c540c-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c540c-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c540c-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="c540c-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c540c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c540c-114">Remarks</span></span>

<span data-ttu-id="c540c-115">Diese Methode multipliziert die gegebene Matrix mit der aktuellen Matrix (die Transformation bezieht sich auf den lokalen Ursprung des Objekts).</span><span class="sxs-lookup"><span data-stu-id="c540c-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="c540c-116">Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der angegebenen Matrix und der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="c540c-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="c540c-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c540c-117">Requirements</span></span>



| <span data-ttu-id="c540c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c540c-118">Requirement</span></span> | <span data-ttu-id="c540c-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c540c-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c540c-120">Header</span><span class="sxs-lookup"><span data-stu-id="c540c-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c540c-121"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="c540c-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c540c-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c540c-122">Library</span></span><br/> | <dl> <span data-ttu-id="c540c-123"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c540c-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c540c-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c540c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c540c-125">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="c540c-125">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="c540c-126">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="c540c-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
