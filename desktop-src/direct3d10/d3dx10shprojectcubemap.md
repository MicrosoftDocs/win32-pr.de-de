---
description: Projiziert eine in einer cubemap dargestellte Funktion in sphärischen Harmonics.
ms.assetid: de8bc4bd-cb29-44ab-8806-33d3ffd10a7b
title: D3DX10SHProjectCubeMap-Funktion (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10SHProjectCubeMap
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fd991e2207f1ad556d9f9b5e648e296b857e884b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353366"
---
# <a name="d3dx10shprojectcubemap-function"></a><span data-ttu-id="9d3ba-103">D3DX10SHProjectCubeMap-Funktion</span><span class="sxs-lookup"><span data-stu-id="9d3ba-103">D3DX10SHProjectCubeMap function</span></span>

<span data-ttu-id="9d3ba-104">Projiziert eine in einer cubemap dargestellte Funktion in sphärischen Harmonics.</span><span class="sxs-lookup"><span data-stu-id="9d3ba-104">Projects a function represented in a cube map into spherical harmonics.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d3ba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d3ba-105">Syntax</span></span>


```C++
HRESULT D3DX10SHProjectCubeMap(
   UINT            Order,
   ID3D10Texture2D *pCubeMap,
   FLOAT           *pROut,
   FLOAT           *pGOut,
   FLOAT           *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="9d3ba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d3ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d3ba-107">*Order*</span><span class="sxs-lookup"><span data-stu-id="9d3ba-107">*Order*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3ba-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d3ba-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9d3ba-109">Reihenfolge der SH-Auswertung, generiert Order ^ 2-coefs, Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="9d3ba-109">Order of the SH evaluation, generates Order^2 coefs, degree is Order-1.</span></span>

</dd> <dt>

<span data-ttu-id="9d3ba-110">*pcubemap*</span><span class="sxs-lookup"><span data-stu-id="9d3ba-110">*pCubeMap*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3ba-111">Typ: **[ **ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span><span class="sxs-lookup"><span data-stu-id="9d3ba-111">Type: **[**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d)\***</span></span>

<span data-ttu-id="9d3ba-112">Cubemap, die in sphärischen Harmoniken projiziert wird.</span><span class="sxs-lookup"><span data-stu-id="9d3ba-112">Cubemap that is going to be projected into spherical harmonics.</span></span> <span data-ttu-id="9d3ba-113">Siehe [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span><span class="sxs-lookup"><span data-stu-id="9d3ba-113">See [**ID3D10Texture2D**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d).</span></span>

</dd> <dt>

<span data-ttu-id="9d3ba-114">*Proxy*</span><span class="sxs-lookup"><span data-stu-id="9d3ba-114">*pROut*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3ba-115">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d3ba-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9d3ba-116">Ausgabe SH-Vektor für rot.</span><span class="sxs-lookup"><span data-stu-id="9d3ba-116">Output SH vector for red.</span></span>

</dd> <dt>

<span data-ttu-id="9d3ba-117">*pgout*</span><span class="sxs-lookup"><span data-stu-id="9d3ba-117">*pGOut*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3ba-118">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d3ba-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9d3ba-119">Ausgabe SH-Vektor für grün.</span><span class="sxs-lookup"><span data-stu-id="9d3ba-119">Output SH vector for green.</span></span>

</dd> <dt>

<span data-ttu-id="9d3ba-120">*pbout*</span><span class="sxs-lookup"><span data-stu-id="9d3ba-120">*pBOut*</span></span> 
</dt> <dd>

<span data-ttu-id="9d3ba-121">Typ: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="9d3ba-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9d3ba-122">Ausgabe SH-Vektor für blau.</span><span class="sxs-lookup"><span data-stu-id="9d3ba-122">Output SH vector for blue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d3ba-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d3ba-123">Return value</span></span>

<span data-ttu-id="9d3ba-124">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9d3ba-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9d3ba-125">Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="9d3ba-125">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d3ba-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d3ba-126">Requirements</span></span>



| <span data-ttu-id="9d3ba-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d3ba-127">Requirement</span></span> | <span data-ttu-id="9d3ba-128">Wert</span><span class="sxs-lookup"><span data-stu-id="9d3ba-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3ba-129">Header</span><span class="sxs-lookup"><span data-stu-id="9d3ba-129">Header</span></span><br/>  | <dl> <span data-ttu-id="9d3ba-130"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d3ba-130"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="9d3ba-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9d3ba-131">Library</span></span><br/> | <dl> <span data-ttu-id="9d3ba-132"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d3ba-132"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9d3ba-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d3ba-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d3ba-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="9d3ba-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
