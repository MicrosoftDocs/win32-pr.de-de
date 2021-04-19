---
description: Berechnet den direkten Beleuchtungs Beitrag zu 3D-Objekten, bei denen die Quell Ausstrahlung durch eine kugelförmige Näherung (SH) dargestellt wird.
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: 'ID3DXPRTEngine:: computedirectlightingsh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357286"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a><span data-ttu-id="a5561-103">ID3DXPRTEngine:: computedirectlightingsh-Methode</span><span class="sxs-lookup"><span data-stu-id="a5561-103">ID3DXPRTEngine::ComputeDirectLightingSH method</span></span>

<span data-ttu-id="a5561-104">Berechnet den direkten Beleuchtungs Beitrag zu 3D-Objekten, bei denen die Quell Ausstrahlung durch eine kugelförmige Näherung (SH) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a5561-104">Computes the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5561-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5561-105">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="a5561-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5561-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5561-107">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5561-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5561-108">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5561-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5561-109">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="a5561-109">Order of the SH evaluation.</span></span> <span data-ttu-id="a5561-110">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="a5561-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a5561-111">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a5561-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a5561-112">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="a5561-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a5561-113">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a5561-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5561-114">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a5561-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a5561-115">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das den direkten Beleuchtungs Beitrag mit der SH-Näherung modelliert.</span><span class="sxs-lookup"><span data-stu-id="a5561-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models the direct lighting contribution with the SH approximation.</span></span> <span data-ttu-id="a5561-116">Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="a5561-116">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5561-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5561-117">Return value</span></span>

<span data-ttu-id="a5561-118">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5561-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5561-119">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5561-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a5561-120">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="a5561-120">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5561-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5561-121">Remarks</span></span>

<span data-ttu-id="a5561-122">Die Ausgabe enthält nicht Albedo, und nur das eingehende Licht ist in den Simulator integriert.</span><span class="sxs-lookup"><span data-stu-id="a5561-122">The output does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="a5561-123">Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.</span><span class="sxs-lookup"><span data-stu-id="a5561-123">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="a5561-124">Rufen Sie [**ID3DXPRTEngine:: multiplyalbedo**](id3dxprtengine--multiplyalbedo.md) auf, um jeden PRT-Vektor (preberechneten Radiance Transfer) von Albedo zu multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="a5561-124">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5561-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5561-125">Requirements</span></span>



| <span data-ttu-id="a5561-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5561-126">Requirement</span></span> | <span data-ttu-id="a5561-127">Wert</span><span class="sxs-lookup"><span data-stu-id="a5561-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5561-128">Header</span><span class="sxs-lookup"><span data-stu-id="a5561-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a5561-129"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5561-129"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a5561-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5561-130">Library</span></span><br/> | <dl> <span data-ttu-id="a5561-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5561-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a5561-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5561-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5561-133">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a5561-133">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
