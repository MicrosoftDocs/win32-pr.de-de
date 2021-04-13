---
description: Berechnet den Quell Strahl, der sich aus einem einzelnen Sprung der interreflektierten hell ergibt. Diese Methode kann für jede beleuchtete Szene verwendet werden, einschließlich eines auf einer kugelförmigen Harmonika (SH) basierenden PRT-Modells.
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'ID3DXPRTEngine:: computebounce-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355706"
---
# <a name="id3dxprtenginecomputebounce-method"></a><span data-ttu-id="af8ef-104">ID3DXPRTEngine:: computebounce-Methode</span><span class="sxs-lookup"><span data-stu-id="af8ef-104">ID3DXPRTEngine::ComputeBounce method</span></span>

<span data-ttu-id="af8ef-105">Berechnet den Quell Strahl, der sich aus einem einzelnen Sprung der interreflektierten hell ergibt.</span><span class="sxs-lookup"><span data-stu-id="af8ef-105">Computes the source radiance resulting from a single bounce of interreflected light.</span></span> <span data-ttu-id="af8ef-106">Diese Methode kann für jede beleuchtete Szene verwendet werden, einschließlich eines auf einer kugelförmigen Harmonika (SH) basierenden PRT-Modells.</span><span class="sxs-lookup"><span data-stu-id="af8ef-106">This method can be used for any lit scene, including a spherical harmonic (SH)-based precomputed radiance transfer (PRT) model.</span></span>

## <a name="syntax"></a><span data-ttu-id="af8ef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="af8ef-107">Syntax</span></span>


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a><span data-ttu-id="af8ef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="af8ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af8ef-109">*pdatain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af8ef-109">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af8ef-110">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="af8ef-110">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="af8ef-111">Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das das 3D-Objekt aus dem vorherigen Licht Sprung darstellt.</span><span class="sxs-lookup"><span data-stu-id="af8ef-111">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span> <span data-ttu-id="af8ef-112">Dieser Eingabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="af8ef-112">This input buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="af8ef-113">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="af8ef-113">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af8ef-114">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="af8ef-114">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="af8ef-115">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das einen einzelnen Sprung des interreflektierten Lichts modelliert.</span><span class="sxs-lookup"><span data-stu-id="af8ef-115">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that models a single bounce of the interreflected light.</span></span> <span data-ttu-id="af8ef-116">Dieser Ausgabepuffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="af8ef-116">This output buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> <dt>

<span data-ttu-id="af8ef-117">*pdatatotal* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="af8ef-117">*pDataTotal* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="af8ef-118">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="af8ef-118">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="af8ef-119">Zeiger auf ein optionales [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, bei dem es sich um die laufende Summe aller vorherigen pdataout-Ausgaben handelt.</span><span class="sxs-lookup"><span data-stu-id="af8ef-119">Pointer to an optional [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that is the running sum of all previous pDataOut outputs.</span></span> <span data-ttu-id="af8ef-120">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="af8ef-120">May be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af8ef-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="af8ef-121">Return value</span></span>

<span data-ttu-id="af8ef-122">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af8ef-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af8ef-123">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af8ef-123">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="af8ef-124">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="af8ef-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="af8ef-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af8ef-125">Remarks</span></span>

<span data-ttu-id="af8ef-126">Verwenden Sie die folgende Aufruf Sequenz, um mehrere Licht Sprünge mit direkter Beleuchtung zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="af8ef-126">Use the following calling sequence to model multiple light bounces with direct lighting.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



<span data-ttu-id="af8ef-127">Verwenden Sie die folgende Aufruf Sequenz, um mehrere Licht Sprünge mit unter Oberflächendaten zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="af8ef-127">Use the following calling sequence to model multiple light bounces with subsurface scattering.</span></span>


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



<span data-ttu-id="af8ef-128">Die Ausgabe dieser Methode enthält nicht "Albedo", und nur das eingehende Licht ist in den Simulator integriert.</span><span class="sxs-lookup"><span data-stu-id="af8ef-128">The output of this method does not include albedo, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="af8ef-129">Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.</span><span class="sxs-lookup"><span data-stu-id="af8ef-129">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="af8ef-130">[**ID3DXPRTEngine:: multiplyalbedo**](id3dxprtengine--multiplyalbedo.md) aufzurufen, um jeden PRT-Vektor von Albedo zu multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="af8ef-130">Call [**ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each PRT vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="af8ef-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af8ef-131">Requirements</span></span>



| <span data-ttu-id="af8ef-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="af8ef-132">Requirement</span></span> | <span data-ttu-id="af8ef-133">Wert</span><span class="sxs-lookup"><span data-stu-id="af8ef-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af8ef-134">Header</span><span class="sxs-lookup"><span data-stu-id="af8ef-134">Header</span></span><br/>  | <dl> <span data-ttu-id="af8ef-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="af8ef-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="af8ef-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="af8ef-136">Library</span></span><br/> | <dl> <span data-ttu-id="af8ef-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af8ef-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af8ef-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="af8ef-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af8ef-139">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="af8ef-139">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="af8ef-140">**ID3DXPRTEngine:: computess**</span><span class="sxs-lookup"><span data-stu-id="af8ef-140">**ID3DXPRTEngine::ComputeSS**</span></span>](id3dxprtengine--computess.md)
</dt> </dl>

 

 




