---
description: Legt ein Array nicht umsetzbarer Matrizen fest.
ms.assetid: 008de62c-3a36-4499-8a0b-9075756395e9
title: 'ID3DXBaseEffect:: setmatrixarray-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrixArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c48dcb3288930a9170c932f335a4b20c258acbb4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354106"
---
# <a name="id3dxbaseeffectsetmatrixarray-method"></a><span data-ttu-id="7e4ab-103">ID3DXBaseEffect:: setmatrixarray-Methode</span><span class="sxs-lookup"><span data-stu-id="7e4ab-103">ID3DXBaseEffect::SetMatrixArray method</span></span>

<span data-ttu-id="7e4ab-104">Legt ein Array nicht umsetzbarer Matrizen fest.</span><span class="sxs-lookup"><span data-stu-id="7e4ab-104">Sets an array of nontransposed matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e4ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e4ab-105">Syntax</span></span>


```C++
HRESULT SetMatrixArray(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix,
  [in]       UINT       Count
);
```



## <a name="parameters"></a><span data-ttu-id="7e4ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e4ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e4ab-107">*hparameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e4ab-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4ab-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="7e4ab-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="7e4ab-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7e4ab-109">Unique identifier.</span></span> <span data-ttu-id="7e4ab-110">Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="7e4ab-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e4ab-111">*pmatrix* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e4ab-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4ab-112">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="7e4ab-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="7e4ab-113">Array nicht umsetzbarer Matrizen.</span><span class="sxs-lookup"><span data-stu-id="7e4ab-113">Array of nontransposed matrices.</span></span> <span data-ttu-id="7e4ab-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="7e4ab-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> <dt>

<span data-ttu-id="7e4ab-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e4ab-115">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e4ab-116">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e4ab-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7e4ab-117">Anzahl von Matrizen im Array.</span><span class="sxs-lookup"><span data-stu-id="7e4ab-117">Number of matrices in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e4ab-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e4ab-118">Return value</span></span>

<span data-ttu-id="7e4ab-119">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e4ab-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e4ab-120">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7e4ab-120">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7e4ab-121">Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.</span><span class="sxs-lookup"><span data-stu-id="7e4ab-121">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e4ab-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e4ab-122">Remarks</span></span>

<span data-ttu-id="7e4ab-123">Eine nicht umgesetzte Matrix enthält Zeilen Hauptdaten; Das heißt, jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="7e4ab-123">A nontransposed matrix contains row-major data; that is, each vector is contained in a row.</span></span>

<span data-ttu-id="7e4ab-124">Wenn die Ziel Matrizen kleiner als die Quell Matrizen sind, werden die zusätzlichen Komponenten der Quell Matrizen ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7e4ab-124">If the destination matrices are smaller than the source matrices, the additional components of the source matrices will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e4ab-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e4ab-125">Requirements</span></span>



| <span data-ttu-id="7e4ab-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e4ab-126">Requirement</span></span> | <span data-ttu-id="7e4ab-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7e4ab-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e4ab-128">Header</span><span class="sxs-lookup"><span data-stu-id="7e4ab-128">Header</span></span><br/>  | <dl> <span data-ttu-id="7e4ab-129"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e4ab-129"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="7e4ab-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7e4ab-130">Library</span></span><br/> | <dl> <span data-ttu-id="7e4ab-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e4ab-131"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7e4ab-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e4ab-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e4ab-133">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="7e4ab-133">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="7e4ab-134">**Getmatrixarray**</span><span class="sxs-lookup"><span data-stu-id="7e4ab-134">**GetMatrixArray**</span></span>](id3dxbaseeffect--getmatrixarray.md)
</dt> </dl>

 

 
