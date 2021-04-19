---
description: Projiziert eine Funktion, die in einer cubemap dargestellt wird, in sphärischen Oberschwingungen (SH).
ms.assetid: da5a3195-801e-4f1c-b52c-9eafc6e2e7b4
title: D3DXSHProjectCubeMap-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHProjectCubeMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0e3e45b42907c47d8c7f1b9e5294738b8997cd6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353753"
---
# <a name="d3dxshprojectcubemap-function"></a><span data-ttu-id="a4620-103">D3DXSHProjectCubeMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="a4620-103">D3DXSHProjectCubeMap function</span></span>

<span data-ttu-id="a4620-104">Projiziert eine Funktion, die in einer cubemap dargestellt wird, in sphärischen Oberschwingungen (SH).</span><span class="sxs-lookup"><span data-stu-id="a4620-104">Projects a function represented on a cube map into spherical harmonics (SH).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4620-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4620-105">Syntax</span></span>


```C++
HRESULT D3DXSHProjectCubeMap(
  _In_ UINT                   Order,
  _In_ LPDIRECT3DCUBETEXTURE9 pCubeMap,
  _In_ FLOAT                  *pROut,
  _In_ FLOAT                  *pGOut,
  _In_ FLOAT                  *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="a4620-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4620-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4620-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4620-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4620-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a4620-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a4620-109">Reihenfolge der Auswertung der sphärischen Harmonika (SH).</span><span class="sxs-lookup"><span data-stu-id="a4620-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="a4620-110">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="a4620-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a4620-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a4620-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a4620-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="a4620-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a4620-113">*pcubemap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4620-113">*pCubeMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4620-114">Typ: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span><span class="sxs-lookup"><span data-stu-id="a4620-114">Type: **[**LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)**</span></span>

<span data-ttu-id="a4620-115">Zeiger auf eine quellcubetextur.</span><span class="sxs-lookup"><span data-stu-id="a4620-115">Pointer to a source cube texture.</span></span> <span data-ttu-id="a4620-116">Siehe [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span><span class="sxs-lookup"><span data-stu-id="a4620-116">See [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9).</span></span>

</dd> <dt>

<span data-ttu-id="a4620-117">*Proxy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4620-117">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4620-118">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4620-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a4620-119">Zeiger auf den Ausgabe-SH-Vektor für die rote Komponente.</span><span class="sxs-lookup"><span data-stu-id="a4620-119">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="a4620-120">*pgout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4620-120">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4620-121">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4620-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a4620-122">Zeiger auf den Ausgabe-SH-Vektor für die grüne Komponente.</span><span class="sxs-lookup"><span data-stu-id="a4620-122">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="a4620-123">*pbout* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a4620-123">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4620-124">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a4620-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a4620-125">Zeiger auf den Ausgabe-SH-Vektor für die blaue Komponente.</span><span class="sxs-lookup"><span data-stu-id="a4620-125">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4620-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4620-126">Return value</span></span>

<span data-ttu-id="a4620-127">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a4620-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a4620-128">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a4620-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a4620-129">Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.</span><span class="sxs-lookup"><span data-stu-id="a4620-129">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4620-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4620-130">Requirements</span></span>



| <span data-ttu-id="a4620-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4620-131">Requirement</span></span> | <span data-ttu-id="a4620-132">Wert</span><span class="sxs-lookup"><span data-stu-id="a4620-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4620-133">Header</span><span class="sxs-lookup"><span data-stu-id="a4620-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a4620-134"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4620-134"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="a4620-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4620-135">Library</span></span><br/> | <dl> <span data-ttu-id="a4620-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4620-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4620-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4620-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4620-138">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a4620-138">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="a4620-139">Voraus berechnete Strahlungs Übertragung (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a4620-139">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
