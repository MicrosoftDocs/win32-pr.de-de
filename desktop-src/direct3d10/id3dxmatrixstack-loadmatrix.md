---
description: 'ID3DXMATRIXStack::LoadMatrix-Methode (D3DX10.h): Lädt die gegebene Matrix in die aktuelle Matrix.'
ms.assetid: b898f344-db90-48e0-b457-0eb8d7b31dca
title: ID3DXMATRIXStack::LoadMatrix-Methode (D3DX10.h)
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
ms.openlocfilehash: 20c80f578abd5e35c89f3ecccedd2ab7fd59e812
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107958"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx10h"></a><span data-ttu-id="ca789-103">ID3DXMATRIXStack::LoadMatrix-Methode (D3DX10.h)</span><span class="sxs-lookup"><span data-stu-id="ca789-103">ID3DXMATRIXStack::LoadMatrix method (D3DX10.h)</span></span>

<span data-ttu-id="ca789-104">Lädt die gegebene Matrix in die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="ca789-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca789-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca789-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="ca789-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca789-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca789-107">*pM* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ca789-107">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca789-108">Typ: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="ca789-108">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="ca789-109">Zeiger auf die in die aktuelle Matrix geladene D3DXMATRIX-Struktur.</span><span class="sxs-lookup"><span data-stu-id="ca789-109">Pointer to the D3DXMATRIX structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca789-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca789-110">Return value</span></span>

<span data-ttu-id="ca789-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ca789-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ca789-112">Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ca789-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ca789-113">Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="ca789-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca789-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca789-114">Remarks</span></span>

<span data-ttu-id="ca789-115">Beachten Sie, dass diese Methode dem Stapel kein Element hinzufüge. stattdessen wird die aktuelle Matrix durch die angegebene Matrix ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ca789-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca789-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca789-116">Requirements</span></span>



| <span data-ttu-id="ca789-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca789-117">Requirement</span></span> | <span data-ttu-id="ca789-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ca789-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca789-119">Header</span><span class="sxs-lookup"><span data-stu-id="ca789-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ca789-120"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="ca789-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca789-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca789-121">Library</span></span><br/> | <dl> <span data-ttu-id="ca789-122"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca789-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca789-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ca789-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca789-124">ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="ca789-124">ID3DXMatrixStack</span></span>](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="ca789-125">D3DX-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="ca789-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
