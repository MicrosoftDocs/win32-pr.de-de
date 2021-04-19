---
description: Ruft eine nicht übersetzte Matrix ab.
ms.assetid: d507c82c-b1a5-4e83-8921-5d45f52faba0
title: 'ID3DXBaseEffect:: getMatrix-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 17d59700d8752526f3f4c48efeaf7f3e6bd985bb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106360239"
---
# <a name="id3dxbaseeffectgetmatrix-method"></a><span data-ttu-id="52736-103">ID3DXBaseEffect:: getMatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="52736-103">ID3DXBaseEffect::GetMatrix method</span></span>

<span data-ttu-id="52736-104">Ruft eine nicht übersetzte Matrix ab.</span><span class="sxs-lookup"><span data-stu-id="52736-104">Gets a nontransposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="52736-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="52736-105">Syntax</span></span>


```C++
HRESULT GetMatrix(
  [in]  D3DXHANDLE hParameter,
  [out] D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="52736-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="52736-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52736-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="52736-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52736-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="52736-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="52736-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="52736-109">Unique identifier.</span></span> <span data-ttu-id="52736-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="52736-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="52736-111">*pmatrix* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="52736-111">*pMatrix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52736-112">Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="52736-112">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="52736-113">Gibt eine nicht übersetzte Matrix zurück.</span><span class="sxs-lookup"><span data-stu-id="52736-113">Returns a nontransposed matrix.</span></span> <span data-ttu-id="52736-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="52736-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52736-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="52736-115">Return value</span></span>

<span data-ttu-id="52736-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="52736-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="52736-117">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52736-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="52736-118">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="52736-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="52736-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52736-119">Remarks</span></span>

<span data-ttu-id="52736-120">Eine nicht umgesetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="52736-120">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="52736-121">Wenn die Ziel Matrix größer als die Quell Matrix ist, werden nur die linken oberen Komponenten der Ziel Matrix gefüllt, und die restlichen Komponenten werden auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="52736-121">If the destination matrix is larger than the source matrix, only the upper-left components of the destination matrix will be filled, and the remaining components will be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="52736-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="52736-122">Requirements</span></span>



| <span data-ttu-id="52736-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="52736-123">Requirement</span></span> | <span data-ttu-id="52736-124">Wert</span><span class="sxs-lookup"><span data-stu-id="52736-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="52736-125">Header</span><span class="sxs-lookup"><span data-stu-id="52736-125">Header</span></span><br/>  | <dl> <span data-ttu-id="52736-126"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="52736-126"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="52736-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="52736-127">Library</span></span><br/> | <dl> <span data-ttu-id="52736-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52736-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="52736-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52736-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52736-130">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="52736-130">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="52736-131">**SetMatrix**</span><span class="sxs-lookup"><span data-stu-id="52736-131">**SetMatrix**</span></span>](id3dxbaseeffect--setmatrix.md)
</dt> </dl>

 

 




