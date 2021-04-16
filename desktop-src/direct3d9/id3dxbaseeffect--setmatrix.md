---
description: Legt eine nicht übersetzte Matrix fest.
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'ID3DXBaseEffect:: setMatrix-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 39a5aed1d6321cf0599d212222fd967ee512e20e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530848"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="e71d9-103">ID3DXBaseEffect:: setMatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="e71d9-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="e71d9-104">Legt eine nicht übersetzte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="e71d9-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="e71d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e71d9-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="e71d9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e71d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71d9-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e71d9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e71d9-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e71d9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e71d9-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e71d9-109">Unique identifier.</span></span> <span data-ttu-id="e71d9-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="e71d9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="e71d9-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e71d9-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e71d9-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e71d9-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e71d9-113">Zeiger auf eine nicht umgesetzte Matrix.</span><span class="sxs-lookup"><span data-stu-id="e71d9-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="e71d9-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="e71d9-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e71d9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e71d9-115">Return value</span></span>

<span data-ttu-id="e71d9-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e71d9-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e71d9-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e71d9-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e71d9-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="e71d9-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e71d9-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e71d9-119">Remarks</span></span>

<span data-ttu-id="e71d9-120">Eine nicht übersetzte Matrix enthält Zeilen Hauptdaten.</span><span class="sxs-lookup"><span data-stu-id="e71d9-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="e71d9-121">Mit anderen Worten: jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="e71d9-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="e71d9-122">Wenn die Ziel Matrix kleiner als die Quell Matrix ist, werden die zusätzlichen Komponenten der Quell Matrix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e71d9-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="e71d9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e71d9-123">Requirements</span></span>



| <span data-ttu-id="e71d9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e71d9-124">Requirement</span></span> | <span data-ttu-id="e71d9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="e71d9-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e71d9-126">Header</span><span class="sxs-lookup"><span data-stu-id="e71d9-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e71d9-127"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="e71d9-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e71d9-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e71d9-128">Library</span></span><br/> | <dl> <span data-ttu-id="e71d9-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e71d9-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e71d9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e71d9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71d9-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e71d9-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="e71d9-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="e71d9-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




