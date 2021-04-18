---
description: Berechnet lokal Aufzähl Bare (ldprt-) Koeffizienten (ldprt)-Koeffizienten in Relation zu pro-Sample-normal Vektoren, um den Fehler der geringsten Quadrate in Bezug auf Eingabe ID3DXPRTBuffer Daten zu minimieren.
ms.assetid: 302c20cd-d495-4a23-9692-7456355471eb
title: 'ID3DXPRTEngine:: computeldprtcoeffs-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeLDPRTCoeffs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 351ecb8022e06b1a5a24abad8fa8541798d13ba0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365869"
---
# <a name="id3dxprtenginecomputeldprtcoeffs-method"></a><span data-ttu-id="01189-103">ID3DXPRTEngine:: computeldprtcoeffs-Methode</span><span class="sxs-lookup"><span data-stu-id="01189-103">ID3DXPRTEngine::ComputeLDPRTCoeffs method</span></span>

<span data-ttu-id="01189-104">Berechnet lokal Aufzähl Bare (ldprt-) Koeffizienten (ldprt)-Koeffizienten in Relation zu pro-Sample-normal Vektoren, um den Fehler der geringsten Quadrate in Bezug auf Eingabe [**ID3DXPRTBuffer**](id3dxprtbuffer.md) Daten zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="01189-104">Computes locally-deformable precomputed radiance transfer (LDPRT) coefficients relative to per-sample normal vectors to minimize the least-squares error with respect to input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) data.</span></span> <span data-ttu-id="01189-105">Diese Koeffizienten können mit häufenden oder transformierten normalen Vektoren verwendet werden, um globale Effekte auf dynamische Objekte zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="01189-105">These coefficients can be used with skinned or transformed normal vectors to model global effects on dynamic objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="01189-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="01189-106">Syntax</span></span>


```C++
HRESULT ComputeLDPRTCoeffs(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      UINT            Order,
  [in, out] D3DXVECTOR3     *pNormOut,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="01189-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="01189-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01189-108">*pdatain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01189-108">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01189-109">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="01189-109">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="01189-110">Zeiger auf das PRT-Datenobjekt (input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) Kugel harmonisch (SH) (SH).</span><span class="sxs-lookup"><span data-stu-id="01189-110">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) spherical harmonic (SH) precomputed radiance transfer (PRT) data object.</span></span>

</dd> <dt>

<span data-ttu-id="01189-111">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01189-111">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01189-112">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="01189-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="01189-113">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="01189-113">Order of the SH evaluation.</span></span> <span data-ttu-id="01189-114">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="01189-114">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="01189-115">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="01189-115">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="01189-116">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="01189-116">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="01189-117">*pnormout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="01189-117">*pNormOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01189-118">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="01189-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="01189-119">Optionales Vektor Array, das mit shaderoptimalen normalen Vektoren gefüllt werden soll, für die ldprt-Koeffizienten optimiert werden.</span><span class="sxs-lookup"><span data-stu-id="01189-119">Optional vector array to be filled with shader-optimal normal vectors for which LDPRT coefficients are optimized.</span></span> <span data-ttu-id="01189-120">Dieses Array muss dieselbe Größe wie die Anzahl der Samplings in pdatain aufweisen.</span><span class="sxs-lookup"><span data-stu-id="01189-120">This array must be the same size as the number of samples in pDataIn.</span></span> <span data-ttu-id="01189-121">Wenn der Wert **null** ist, werden Oberflächen normale Vektoren verwendet.</span><span class="sxs-lookup"><span data-stu-id="01189-121">If **NULL**, surface normal vectors are used.</span></span>

</dd> <dt>

<span data-ttu-id="01189-122">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="01189-122">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="01189-123">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="01189-123">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="01189-124">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das die Reihenfolge der harmonischen Koeffizient pro Farbkanal pro Beispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="01189-124">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that contains Order zonal harmonic coefficients per color channel per sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01189-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="01189-125">Return value</span></span>

<span data-ttu-id="01189-126">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="01189-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="01189-127">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="01189-127">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="01189-128">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="01189-128">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="01189-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01189-129">Remarks</span></span>

<span data-ttu-id="01189-130">Lösungen für Schattierungs normale Vektoren können mit dieser Methode optional abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="01189-130">Solutions for shading normal vectors can optionally be obtained with this method.</span></span> <span data-ttu-id="01189-131">Diese normalen Vektoren können zusammen mit den ldprt-Koeffizienten das PRT-Signal genauer darstellen.</span><span class="sxs-lookup"><span data-stu-id="01189-131">These normal vectors, along with the LDPRT coefficients, can more accurately represent the PRT signal.</span></span> <span data-ttu-id="01189-132">In diesem Fall stellen die Koeffizienten zonale Oberschwingungen dar, die in normaler Richtung ausgerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="01189-132">In this case, the coefficients represent zonal harmonics oriented in the normal direction.</span></span>

<span data-ttu-id="01189-133">Diese Methode kann nicht mit Ergebnissen aus [**ID3DXPRTEngine:: computesurf samplesbounce**](id3dxprtengine--computesurfsamplesbounce.md) oder [**ID3DXPRTEngine:: computesurf samplesdirectsh**](id3dxprtengine--computesurfsamplesdirectsh.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01189-133">This method cannot be used with results from [**ID3DXPRTEngine::ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md) or [**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="01189-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01189-134">Requirements</span></span>



| <span data-ttu-id="01189-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01189-135">Requirement</span></span> | <span data-ttu-id="01189-136">Wert</span><span class="sxs-lookup"><span data-stu-id="01189-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01189-137">Header</span><span class="sxs-lookup"><span data-stu-id="01189-137">Header</span></span><br/>  | <dl> <span data-ttu-id="01189-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="01189-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="01189-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="01189-139">Library</span></span><br/> | <dl> <span data-ttu-id="01189-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01189-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="01189-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01189-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01189-142">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="01189-142">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
