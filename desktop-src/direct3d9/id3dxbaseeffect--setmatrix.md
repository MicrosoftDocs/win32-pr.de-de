---
description: 'ID3DXBaseEffect::SetMatrix-Methode: Legt eine nicht transponierte Matrix fest.'
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: ID3DXBaseEffect::SetMatrix-Methode (D3DX9Shader.h)
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
ms.openlocfilehash: 7af7dc0daa3dcd29e7b15c4fe435b9626ea41746
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097498"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a><span data-ttu-id="fe189-103">ID3DXBaseEffect::SetMatrix-Methode</span><span class="sxs-lookup"><span data-stu-id="fe189-103">ID3DXBaseEffect::SetMatrix method</span></span>

<span data-ttu-id="fe189-104">Legt eine nicht transponierte Matrix fest.</span><span class="sxs-lookup"><span data-stu-id="fe189-104">Sets a non-transposed matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe189-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe189-105">Syntax</span></span>


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="fe189-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe189-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe189-107">*hParameter* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe189-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe189-108">Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fe189-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fe189-109">Eindeutiger Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="fe189-109">Unique identifier.</span></span> <span data-ttu-id="fe189-110">Siehe [Handles (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fe189-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fe189-111">*pMatrix* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="fe189-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe189-112">Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe189-112">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fe189-113">Zeiger auf eine nicht transposed Matrix.</span><span class="sxs-lookup"><span data-stu-id="fe189-113">Pointer to a nontransposed matrix.</span></span> <span data-ttu-id="fe189-114">Siehe [**D3DXMATRIX**](d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="fe189-114">See [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe189-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe189-115">Return value</span></span>

<span data-ttu-id="fe189-116">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fe189-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fe189-117">Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fe189-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fe189-118">Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.</span><span class="sxs-lookup"><span data-stu-id="fe189-118">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe189-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe189-119">Remarks</span></span>

<span data-ttu-id="fe189-120">Eine nicht transponierte Matrix enthält Zeilen-Hauptdaten.</span><span class="sxs-lookup"><span data-stu-id="fe189-120">A non-transposed matrix contains row-major data.</span></span> <span data-ttu-id="fe189-121">Anders ausgedrückt: Jeder Vektor ist in einer Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="fe189-121">In other words, each vector is contained in a row.</span></span>

<span data-ttu-id="fe189-122">Wenn die Zielmatrix kleiner als die Quellmatrix ist, werden die zusätzlichen Komponenten der Quellmatrix ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fe189-122">If the destination matrix is smaller than the source matrix, the additional components of the source matrix will be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe189-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe189-123">Requirements</span></span>



| <span data-ttu-id="fe189-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe189-124">Requirement</span></span> | <span data-ttu-id="fe189-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fe189-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe189-126">Header</span><span class="sxs-lookup"><span data-stu-id="fe189-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fe189-127"><dt>D3DX9Shader.h</dt></span><span class="sxs-lookup"><span data-stu-id="fe189-127"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fe189-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe189-128">Library</span></span><br/> | <dl> <span data-ttu-id="fe189-129"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe189-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fe189-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fe189-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe189-131">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fe189-131">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="fe189-132">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="fe189-132">**GetMatrix**</span></span>](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




