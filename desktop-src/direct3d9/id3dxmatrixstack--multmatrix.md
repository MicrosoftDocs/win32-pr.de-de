---
description: Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.
ms.assetid: a673ce82-6fed-4a3f-8c37-d0db11195f06
title: 'ID3DXMATRIXStack:: mehrtmatrix-Methode (D3dx9math. h)'
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fc9b3fb49387e354645c8a3c09c7572b4da80109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361848"
---
# <a name="id3dxmatrixstackmultmatrix-method-d3dx9mathh"></a><span data-ttu-id="481b3-103">ID3DXMATRIXStack:: mehrtmatrix-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="481b3-103">ID3DXMATRIXStack::MultMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="481b3-104">Bestimmt das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="481b3-104">Determines the product of the current matrix and the given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="481b3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="481b3-105">Syntax</span></span>


```C++
HRESULT MultMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="481b3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="481b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="481b3-107">*pmat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="481b3-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="481b3-108">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="481b3-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="481b3-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die mit der aktuellen Matrix multipliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="481b3-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure to be multiplied with the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="481b3-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="481b3-110">Return value</span></span>

<span data-ttu-id="481b3-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="481b3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="481b3-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="481b3-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="481b3-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="481b3-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="481b3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="481b3-114">Remarks</span></span>

<span data-ttu-id="481b3-115">Diese Methode multipliziert die angegebene Matrix nach rechts mit der aktuellen Matrix (die Transformation geht zum aktuellen Ursprung der Welt).</span><span class="sxs-lookup"><span data-stu-id="481b3-115">This method right-multiplies the given matrix to the current matrix (transformation is about the current world origin).</span></span>


```
m_pstack[m_currentPos] = m_pstack[m_currentPos] * (*pMat);
```



<span data-ttu-id="481b3-116">Diese Methode fügt dem Stapel kein Element hinzu, sondern ersetzt die aktuelle Matrix durch das Produkt der aktuellen Matrix und der angegebenen Matrix.</span><span class="sxs-lookup"><span data-stu-id="481b3-116">This method does not add an item to the stack, it replaces the current matrix with the product of the current matrix and the given matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="481b3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="481b3-117">Requirements</span></span>



| <span data-ttu-id="481b3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="481b3-118">Requirement</span></span> | <span data-ttu-id="481b3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="481b3-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="481b3-120">Header</span><span class="sxs-lookup"><span data-stu-id="481b3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="481b3-121"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="481b3-121"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="481b3-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="481b3-122">Library</span></span><br/> | <dl> <span data-ttu-id="481b3-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="481b3-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="481b3-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="481b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="481b3-125">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="481b3-125">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="481b3-126">**ID3DXMATRIXStack:: mehrtmatrixlocal**</span><span class="sxs-lookup"><span data-stu-id="481b3-126">**ID3DXMATRIXStack::MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)
</dt> </dl>

 

 




