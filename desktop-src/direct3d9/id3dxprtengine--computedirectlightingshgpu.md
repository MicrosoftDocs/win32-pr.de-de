---
description: Verwendet die GPU, um den direkten Beleuchtungs Beitrag zu 3D-Objekten zu berechnen, wobei die Quell Ausstrahlung durch eine Glanz förmige Näherung (SH) dargestellt wird. Das Berechnen der Beleuchtung auf der GPU ist in der Regel viel schneller als auf der CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'ID3DXPRTEngine:: computedirectlightingshgpu-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106365352"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a><span data-ttu-id="a84ef-104">ID3DXPRTEngine:: computedirectlightingshgpu-Methode</span><span class="sxs-lookup"><span data-stu-id="a84ef-104">ID3DXPRTEngine::ComputeDirectLightingSHGPU method</span></span>

<span data-ttu-id="a84ef-105">Verwendet die GPU, um den direkten Beleuchtungs Beitrag zu 3D-Objekten zu berechnen, wobei die Quell Ausstrahlung durch eine Glanz förmige Näherung (SH) dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a84ef-105">Uses the GPU to compute the direct lighting contribution to 3D objects where the source radiance is represented by a spherical harmonic (SH) approximation.</span></span> <span data-ttu-id="a84ef-106">Das Berechnen der Beleuchtung auf der GPU ist in der Regel viel schneller als auf der CPU.</span><span class="sxs-lookup"><span data-stu-id="a84ef-106">Computing the lighting on the GPU will generally be much faster than on the CPU.</span></span>

## <a name="syntax"></a><span data-ttu-id="a84ef-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a84ef-107">Syntax</span></span>


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="a84ef-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a84ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a84ef-109">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a84ef-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a84ef-110">Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a84ef-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a84ef-111">Zeiger auf das [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Geräte Objekt, das verwendet wird, um die Simulation auf der GPU auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a84ef-111">Pointer to the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used to run the simulation on the GPU.</span></span> <span data-ttu-id="a84ef-112">Das Gerät muss [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) Pixel Shader unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a84ef-112">The device must support [ps\_2\_0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) pixel shaders.</span></span>

> [!Note]  
> <span data-ttu-id="a84ef-113">Rückruf Funktionen dürfen nicht das [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Geräte Objekt verwenden, das vom GPU-Simulator verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a84ef-113">Callback functions should not use the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device object used by the GPU simulator.</span></span>

 

</dd> <dt>

<span data-ttu-id="a84ef-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="a84ef-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a84ef-115">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a84ef-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a84ef-116">Der GPU-Simulations Parameter, der die Auflösung des Schatten-z-Puffers definiert.</span><span class="sxs-lookup"><span data-stu-id="a84ef-116">GPU simulation parameter that defines the resolution of the shadow z-buffer.</span></span> <span data-ttu-id="a84ef-117">Muss auf einen der Konstanten Werte aus [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a84ef-117">Should be set to one of the constant values from [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md).</span></span> <span data-ttu-id="a84ef-118">Der D3DXSHGPUSIMOPT \_ HighQuality-Wert kann mit einem der D3DXSHGPUSIMOPT shadowresxxx-Werte kombiniert werden, um die Simulation mit einer höheren Genauigkeit zu spezifiken \_ .</span><span class="sxs-lookup"><span data-stu-id="a84ef-118">To specifiy higher precision simulation, the D3DXSHGPUSIMOPT\_HIGHQUALITY value may be combined with one of the D3DXSHGPUSIMOPT\_SHADOWRESxxx values.</span></span>

</dd> <dt>

<span data-ttu-id="a84ef-119">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a84ef-119">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a84ef-120">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a84ef-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a84ef-121">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="a84ef-121">Order of the SH evaluation.</span></span> <span data-ttu-id="a84ef-122">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="a84ef-122">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="a84ef-123">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="a84ef-123">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="a84ef-124">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="a84ef-124">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="a84ef-125">*Zbias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a84ef-125">*ZBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a84ef-126">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a84ef-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a84ef-127">In normaler Richtung ausrichten.</span><span class="sxs-lookup"><span data-stu-id="a84ef-127">Bias in the normal direction.</span></span>

</dd> <dt>

<span data-ttu-id="a84ef-128">*Zanglebias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a84ef-128">*ZAngleBias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a84ef-129">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a84ef-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a84ef-130">Wird in normaler Richtung gemessen und um eins abzüglich des Kosinus des Winkels mit dem Lichtstrahl skaliert.</span><span class="sxs-lookup"><span data-stu-id="a84ef-130">Bias in the normal direction, scaled by one minus the cosine of the angle with the light ray.</span></span>

</dd> <dt>

<span data-ttu-id="a84ef-131">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a84ef-131">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a84ef-132">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="a84ef-132">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="a84ef-133">Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="a84ef-133">Pointer to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span> <span data-ttu-id="a84ef-134">Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="a84ef-134">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a84ef-135">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a84ef-135">Return value</span></span>

<span data-ttu-id="a84ef-136">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a84ef-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a84ef-137">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a84ef-137">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a84ef-138">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="a84ef-138">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a84ef-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a84ef-139">Remarks</span></span>

<span data-ttu-id="a84ef-140">Bei dieser Methode wird die Albedo-Methode nicht mit dem Lichtsignal multipliziert, und nur das eingehende Licht ist in den Simulator integriert.</span><span class="sxs-lookup"><span data-stu-id="a84ef-140">In this method, the albedo is not multiplied by the light signal, and only incoming light is integrated in the simulator.</span></span> <span data-ttu-id="a84ef-141">Indem Sie Albedo nicht multiplizieren, können Sie Albedo-Variation in einer präziseren Skalierung als die Quell Strahlung modellieren und dadurch genauere Ergebnisse aus der Komprimierung erzielen.</span><span class="sxs-lookup"><span data-stu-id="a84ef-141">By not multiplying the albedo, you can model albedo variation at a finer scale than the source radiance, thereby yielding more accurate results from compression.</span></span>

<span data-ttu-id="a84ef-142">Rufen Sie [**multiplyalbedo**](id3dxprtengine--multiplyalbedo.md) auf, um die einzelnen PRT-Vektoren (preberechneten Radiance Transfer) von Albedo zu multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="a84ef-142">Call [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) to multiply each precomputed radiance transfer (PRT) vector by the albedo.</span></span>

## <a name="requirements"></a><span data-ttu-id="a84ef-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a84ef-143">Requirements</span></span>



| <span data-ttu-id="a84ef-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a84ef-144">Requirement</span></span> | <span data-ttu-id="a84ef-145">Wert</span><span class="sxs-lookup"><span data-stu-id="a84ef-145">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a84ef-146">Header</span><span class="sxs-lookup"><span data-stu-id="a84ef-146">Header</span></span><br/>  | <dl> <span data-ttu-id="a84ef-147"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a84ef-147"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a84ef-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a84ef-148">Library</span></span><br/> | <dl> <span data-ttu-id="a84ef-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a84ef-149"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a84ef-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a84ef-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a84ef-151">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="a84ef-151">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
