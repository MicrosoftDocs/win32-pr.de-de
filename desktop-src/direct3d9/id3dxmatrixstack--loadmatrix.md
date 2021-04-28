---
description: 'ID3DXMATRIXStack::LoadMatrix-Methode (D3dx9math.h): Lädt die angegebene Matrix in die aktuelle Matrix.'
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: ID3DXMATRIXStack::LoadMatrix-Methode (D3dx9math.h)
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
ms.openlocfilehash: f2ee7e5cae4d28b81b805faa4f113d0819f1eae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093538"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a><span data-ttu-id="5feff-103">ID3DXMATRIXStack::LoadMatrix-Methode (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="5feff-103">ID3DXMATRIXStack::LoadMatrix method (D3dx9math.h)</span></span>

<span data-ttu-id="5feff-104">Lädt die angegebene Matrix in die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="5feff-104">Loads the given matrix into the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5feff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5feff-105">Syntax</span></span>


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a><span data-ttu-id="5feff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5feff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5feff-107">*pMat* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="5feff-107">*pMat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5feff-108">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="5feff-108">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="5feff-109">Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die in die aktuelle Matrix geladen wird.</span><span class="sxs-lookup"><span data-stu-id="5feff-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure loaded into the current matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5feff-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5feff-110">Return value</span></span>

<span data-ttu-id="5feff-111">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5feff-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5feff-112">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5feff-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5feff-113">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="5feff-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="5feff-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5feff-114">Remarks</span></span>

<span data-ttu-id="5feff-115">Beachten Sie, dass diese Methode dem Stapel kein Element hinzufüge. stattdessen wird die aktuelle Matrix durch die angegebene Matrix ersetzt.</span><span class="sxs-lookup"><span data-stu-id="5feff-115">Note that this method does not add an item to the stack; rather, it replaces the current matrix with the supplied matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="5feff-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5feff-116">Requirements</span></span>



| <span data-ttu-id="5feff-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5feff-117">Requirement</span></span> | <span data-ttu-id="5feff-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5feff-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5feff-119">Header</span><span class="sxs-lookup"><span data-stu-id="5feff-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5feff-120"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="5feff-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5feff-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5feff-121">Library</span></span><br/> | <dl> <span data-ttu-id="5feff-122"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5feff-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5feff-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5feff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5feff-124">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="5feff-124">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="5feff-125">**ID3DXMATRIXStack::LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="5feff-125">**ID3DXMATRIXStack::LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




