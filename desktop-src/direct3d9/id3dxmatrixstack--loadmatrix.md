---
description: Lädt die angegebene Matrix in die aktuelle Matrix.
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'ID3DXMATRIXStack:: loadmatrix-Methode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 292b4e147dfa99023f0b4d560a4ed41e6b41b3fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530860"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="33071-103">ID3DXMATRIXStack:: loadmatrix-Methode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="33071-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="33071-104">Lädt die angegebene Matrix in die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="33071-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="33071-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="33071-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="33071-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="33071-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33071-107">*pmat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33071-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33071-108">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="33071-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="33071-109">Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die in die aktuelle Matrix geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="33071-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33071-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="33071-110">Return value</span></span>

<span data-ttu-id="33071-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="33071-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="33071-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="33071-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="33071-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="33071-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="33071-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33071-114">Remarks</span></span>

<span data-ttu-id="33071-115">Beachten Sie, dass diese Methode dem Stapel kein Element hinzufügt. Stattdessen wird die aktuelle Matrix durch die angegebene Matrix ersetzt.</span><span class="sxs-lookup"><span data-stu-id="33071-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="33071-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33071-116">Requirements</span></span>



| <span data-ttu-id="33071-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33071-117">Requirement</span></span> | <span data-ttu-id="33071-118">Wert</span><span class="sxs-lookup"><span data-stu-id="33071-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="33071-119">Header</span><span class="sxs-lookup"><span data-stu-id="33071-119">Header</span></span><br/>  | <dl> <span data-ttu-id="33071-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="33071-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="33071-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="33071-121">Library</span></span><br/> | <dl> <span data-ttu-id="33071-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33071-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="33071-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33071-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33071-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="33071-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="33071-125">**ID3DXMATRIXStack:: loadidentity**</span><span class="sxs-lookup"><span data-stu-id="33071-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




