---
description: Berechnet eine Projektion der direkten Beleuchtung aus dem vorherigen Licht Sprung in eine kugelförmige (SH) Basis Vektoren, die den Vorfall Glanz an angegebenen Orten darstellen.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: 'ID3DXPRTEngine:: computevolumesamples-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bd77fff723f0cf7e3dc2a52be6a40ff6f0d71fe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361238"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a><span data-ttu-id="c8523-103">ID3DXPRTEngine:: computevolumesamples-Methode</span><span class="sxs-lookup"><span data-stu-id="c8523-103">ID3DXPRTEngine::ComputeVolumeSamples method</span></span>

<span data-ttu-id="c8523-104">Berechnet eine Projektion der direkten Beleuchtung aus dem vorherigen Licht Sprung in eine kugelförmige (SH) Basis Vektoren, die den Vorfall Glanz an angegebenen Orten darstellen.</span><span class="sxs-lookup"><span data-stu-id="c8523-104">Computes a projection of the direct lighting from the previous light bounce into spherical harmonic (SH) basis vectors that represent incident radiance at specified locations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8523-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8523-105">Syntax</span></span>


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a><span data-ttu-id="c8523-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8523-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8523-107">*psurfdatain* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8523-107">*pSurfDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8523-108">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c8523-108">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c8523-109">Zeiger auf ein [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Eingabe Objekt, das das 3D-Objekt aus dem vorherigen Licht Sprung darstellt.</span><span class="sxs-lookup"><span data-stu-id="c8523-109">Pointer to an input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that represents the 3D object from the previous light bounce.</span></span>

</dd> <dt>

<span data-ttu-id="c8523-110">*Reihenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8523-110">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8523-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8523-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8523-112">Die Reihenfolge der SH-Evaluierung.</span><span class="sxs-lookup"><span data-stu-id="c8523-112">Order of the SH evaluation.</span></span> <span data-ttu-id="c8523-113">Muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.</span><span class="sxs-lookup"><span data-stu-id="c8523-113">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="c8523-114">Die Auswertung generiert die Koeffizienten der Bestellung.</span><span class="sxs-lookup"><span data-stu-id="c8523-114">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="c8523-115">Der Bewertungs Grad ist Order-1.</span><span class="sxs-lookup"><span data-stu-id="c8523-115">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="c8523-116">*NumVolSamples.xml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8523-116">*NumVolSamples.xml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8523-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8523-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c8523-118">Anzahl der Beispiel Speicherorte.</span><span class="sxs-lookup"><span data-stu-id="c8523-118">Number of sample locations.</span></span>

</dd> <dt>

<span data-ttu-id="c8523-119">*psamplelocs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8523-119">*pSampleLocs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8523-120">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="c8523-120">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="c8523-121">Die Position für jede Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="c8523-121">Position for each sample.</span></span> <span data-ttu-id="c8523-122">Wenn psamplelocs den Wert **null** hat, berechnet computevolumesamples Übertragungs Matrizen an jedem Mesh-Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="c8523-122">If pSampleLocs is **NULL**, ComputeVolumeSamples will compute transfer matrices at every mesh vertex.</span></span> <span data-ttu-id="c8523-123">Wenn psamplelocs jedoch nicht **null** ist, müssen Sie eine Stichprobe über eine Kugel ausführen (Set usesphere = **true** und usecosinus = **false** in [**ID3DXPRTEngine:: setsamplinginfo**](id3dxprtengine--setsamplinginfo.md)); Andernfalls gibt computevolumesamples D3DERR \_ invalidcallzurück.</span><span class="sxs-lookup"><span data-stu-id="c8523-123">However, if pSampleLocs is not **NULL**, you must sample over a sphere (set UseSphere = **TRUE** and UseCosine = **FALSE** in [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); otherwise, ComputeVolumeSamples will return D3DERR\_INVALIDCALL.</span></span>

</dd> <dt>

<span data-ttu-id="c8523-124">*pdataout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c8523-124">*pDataOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8523-125">Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="c8523-125">Type: **[**LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="c8523-126">Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das die direkte Beleuchtung aus dem vorherigen Licht Sprung in SH-Basis Vektoren projiziert.</span><span class="sxs-lookup"><span data-stu-id="c8523-126">Pointer to an output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object that projects the direct lighting from the previous light bounce into SH basis vectors.</span></span> <span data-ttu-id="c8523-127">Dieser Puffer muss über die richtige Anzahl von Farbkanälen verfügen, die für die Simulation reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="c8523-127">This buffer must have the proper number of color channels allocated for the simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8523-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c8523-128">Return value</span></span>

<span data-ttu-id="c8523-129">Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8523-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8523-130">Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c8523-130">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c8523-131">Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.</span><span class="sxs-lookup"><span data-stu-id="c8523-131">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8523-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8523-132">Remarks</span></span>

<span data-ttu-id="c8523-133">Diese Methode berechnet, wie das Licht aus der Quell Funktions Funktion von der Oberfläche reflektiert wird, die die Szene darstellt (psurfdatain) und an jedem von psamplelocs angegebenen Punkt des Raums ankommt.</span><span class="sxs-lookup"><span data-stu-id="c8523-133">This method computes how the light from the source radiance function is reflected off the surface that represents the scene (pSurfDataIn) and arrives at each point in space specified by pSampleLocs.</span></span> <span data-ttu-id="c8523-134">Die SH-Koeffizienten stellen die Zuordnung der Quell Strahlung an jedem psamplelocs-Punkt zur Übertragung von Ereignis Strahlen dar.</span><span class="sxs-lookup"><span data-stu-id="c8523-134">The SH coefficients represent the mapping, at each pSampleLocs point, of source radiance to transferred incident radiance.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8523-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c8523-135">Requirements</span></span>



| <span data-ttu-id="c8523-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c8523-136">Requirement</span></span> | <span data-ttu-id="c8523-137">Wert</span><span class="sxs-lookup"><span data-stu-id="c8523-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8523-138">Header</span><span class="sxs-lookup"><span data-stu-id="c8523-138">Header</span></span><br/>  | <dl> <span data-ttu-id="c8523-139"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8523-139"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c8523-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c8523-140">Library</span></span><br/> | <dl> <span data-ttu-id="c8523-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8523-141"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c8523-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8523-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8523-143">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="c8523-143">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> <dt>

[<span data-ttu-id="c8523-144">**ID3DXPRTEngine:: computevolumesamplesdirectsh**</span><span class="sxs-lookup"><span data-stu-id="c8523-144">**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**</span></span>](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
