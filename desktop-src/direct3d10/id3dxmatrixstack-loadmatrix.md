---
description: Lädt die angegebene Matrix in die aktuelle Matrix.
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: 'ID3DXMATRIXStack:: loadmatrix-Methode (d3dx10. h)'
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ce6b99abf4c9a82a8b9d1c7643a1098d19e18c15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356016"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="059f9-103">ID3DXMATRIXStack:: loadmatrix-Methode (d3dx10. h)</span><span class="sxs-lookup"><span data-stu-id="059f9-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="059f9-104">Lädt die angegebene Matrix in die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="059f9-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="059f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="059f9-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="059f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="059f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="059f9-107">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="059f9-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="059f9-108">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="059f9-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="059f9-109">Ein Zeiger auf die D3DXMATRIX-Struktur, die in die aktuelle Matrix geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="059f9-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="059f9-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="059f9-110">Return value</span></span>

<span data-ttu-id="059f9-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="059f9-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="059f9-112">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="059f9-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="059f9-113">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="059f9-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="059f9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="059f9-114">Remarks</span></span>

<span data-ttu-id="059f9-115">Beachten Sie, dass diese Methode dem Stapel kein Element hinzufügt. Stattdessen wird die aktuelle Matrix durch die angegebene Matrix ersetzt.</span><span class="sxs-lookup"><span data-stu-id="059f9-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="059f9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="059f9-116">Requirements</span></span>



| <span data-ttu-id="059f9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="059f9-117">Requirement</span></span> | <span data-ttu-id="059f9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="059f9-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="059f9-119">Header</span><span class="sxs-lookup"><span data-stu-id="059f9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="059f9-120"><dt>D3dx10. h</dt></span><span class="sxs-lookup"><span data-stu-id="059f9-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="059f9-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="059f9-121">Library</span></span><br/> | <dl> <span data-ttu-id="059f9-122"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="059f9-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="059f9-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="059f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="059f9-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="059f9-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="059f9-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="059f9-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
