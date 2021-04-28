---
description: 'ID3DXMATRIXStack::MultMatrixLocal-Methode (D3dx9math.h): Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.'
ms.assetid: 6f909b38-821c-4173-aba9-fd4392f70551
title: ID3DXMATRIXStack::MultMatrixLocal-Methode (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 509aff4dd21f62033dc1e4672d29aad57445f9ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093518"
---
# <a name="id3dxmatrixstackmultmatrixlocal-method-d3dx9mathh"></a><span data-ttu-id="d98b0-103">ID3DXMATRIXStack::MultMatrixLocal-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="d98b0-103">ID3DXMATRIXStack::MultMatrixLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="d98b0-104">Bestimmt das Produkt der angegebenen Matrix und der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="d98b0-104">Determines the product of the given matrix and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98b0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d98b0-105">Syntax</span></span>


```C++
HRESULT MultMatrixLocal(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="d98b0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d98b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d98b0-107">*pMat* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="d98b0-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d98b0-108">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="d98b0-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d98b0-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die mit der aktuellen Matrix multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d98b0-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d98b0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d98b0-110">Return value</span></span>

<span data-ttu-id="d98b0-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d98b0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d98b0-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d98b0-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d98b0-113">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="d98b0-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d98b0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d98b0-114">Remarks</span></span>

<span data-ttu-id="d98b0-115">Diese Methode multipliziert die angegebene Matrix links mit der aktuellen Matrix (die Transformation geht um den lokalen Ursprung des Objekts).</span><span class="sxs-lookup"><span data-stu-id="d98b0-115">This method left-multiplies the given matrix to the current matrix (transformation is about the local origin of the object).</span></span>


```
m_pstack[m_currentPos] = (*pMat) * m_pstack[m_currentPos];
```



<span data-ttu-id="d98b0-116">Diese Methode fügt dem Stapel kein Element hinzu. Sie ersetzt die aktuelle Matrix durch das Produkt der angegebenen Matrix und der aktuellen Matrix.</span><span class="sxs-lookup"><span data-stu-id="d98b0-116">This method does not add an item to the stack, it replaces the current matrix with the product of the given matrix and the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="d98b0-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d98b0-117">Requirements</span></span>



| <span data-ttu-id="d98b0-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d98b0-118">Requirement</span></span> | <span data-ttu-id="d98b0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d98b0-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d98b0-120">Header</span><span class="sxs-lookup"><span data-stu-id="d98b0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d98b0-121"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="d98b0-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="d98b0-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d98b0-122">Library</span></span><br/> | <dl> <span data-ttu-id="d98b0-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d98b0-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d98b0-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d98b0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98b0-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="d98b0-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="d98b0-126">**ID3DXMATRIXStack::MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="d98b0-126">**ID3DXMATRIXStack::MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)
</dt> </dl>

 

 




